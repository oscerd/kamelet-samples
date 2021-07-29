# Simulation to MSSQL Server

- This has been tested on Minikube

- Run the following command

    > kubectl run mssql-1 --image=mcr.microsoft.com/mssql/server:2017-latest --port=1433 --env 'ACCEPT_EULA=Y' --env 'SA_PASSWORD=Password!'

- Once the pod is up and running we'll need to create the table and populate it with same starting data

    > kubectl exec -it mssql-1 -- bash
    > root@mssql-1:/# /opt/mssql-tools/bin/sqlcmd -S localhost -U SA -P "Password!"
    1> CREATE TABLE accounts (user_id INT PRIMARY KEY, username VARCHAR ( 50 ) UNIQUE NOT NULL, city VARCHAR ( 50 ) NOT NULL );
    2> GO
    1> INSERT into accounts (user_id,username,city) VALUES (1, 'andrea', 'Roma');
    2> GO
    1> INSERT into accounts (user_id,username,city) VALUES (2, 'John', 'New York');
    2> GO

- So we now have two rows in the database.

- Add the correct credentials and address in the flow-binding yaml for the MSSQL Server database.

- Run the following commands

    kubectl apply -f flow-binding.yaml

- Check logs

    kamel logs simulation-to-sqlserver

You should a first row inserted and then failing inserts because the primary key will be duplicated

If you go back to the postgresql console you won't have any row on the database, because of the consumedQuery parameter

- Now we can check the database

    > kubectl exec -it mssql-1 -- bash
    > root@mssql-1:/# /opt/mssql-tools/bin/sqlcmd -S localhost -U SA -P "Password!"
    1> SELECT * from accounts;
    2> GO
    user_id     username                                           city                                              
    ----------- -------------------------------------------------- --------------------------------------------------
                1 andrea                                             Roma                                              
                2 John                                               New York                                          
                3 Malpensa                                           Roma                                              

    (3 rows affected)

