# Slack Source Example

In this sample you'll use the Slack Source Kamelet

## Setup the Slack Bot App

1. Go to https://api.slack.com/apps and create an app
2. Set the following permissions to this app, in particular in relation to Bot Token
- channels:history
- groups:history
- im:history
- mpim:history
- channels:read
- groups:read
- im:read
- mpim:read
3. Enable incoming webhook for this Bot App
4. Copy the User OAuth Token 
5. Open the slack-integration.properties file and paste the token as token property
6. Set the correct channel name

## Run

Run the following command:

```
> jbang --fresh camel@apache/camel run --properties=slack-integration.properties slack-source.yaml
```

You should see

```
Starting CamelJBang
2022-03-10 14:44:36.588  INFO 10188 --- [           main] e.camel.impl.engine.AbstractCamelContext : Detected: camel-debug JAR (enabling Camel Debugging)
2022-03-10 14:44:36.746  INFO 10188 --- [           main] org.apache.camel.main.BaseMainSupport    : Auto-configuration summary
2022-03-10 14:44:36.746  INFO 10188 --- [           main] org.apache.camel.main.BaseMainSupport    :     camel.component.properties.location=file:///home/oscerd/workspace/miscellanea/kamelet-samples/camel-jbang/slack-source/slack-integration.properties,
2022-03-10 14:44:36.747  INFO 10188 --- [           main] org.apache.camel.main.BaseMainSupport    :     camel.main.name=CamelJBang
2022-03-10 14:44:36.747  INFO 10188 --- [           main] org.apache.camel.main.BaseMainSupport    :     camel.main.shutdownTimeout=5
2022-03-10 14:44:36.747  INFO 10188 --- [           main] org.apache.camel.main.BaseMainSupport    :     camel.main.routesReloadEnabled=false
2022-03-10 14:44:36.747  INFO 10188 --- [           main] org.apache.camel.main.BaseMainSupport    :     camel.main.sourceLocationEnabled=true
2022-03-10 14:44:36.747  INFO 10188 --- [           main] org.apache.camel.main.BaseMainSupport    :     camel.main.tracing=false
2022-03-10 14:44:36.747  INFO 10188 --- [           main] org.apache.camel.main.BaseMainSupport    :     camel.main.routesIncludePattern=file:slack-source.yaml
2022-03-10 14:44:36.747  INFO 10188 --- [           main] org.apache.camel.main.BaseMainSupport    :     camel.component.kamelet.location=classpath:/kamelets,github:apache:camel-kamelets/kamelets
2022-03-10 14:44:36.840  INFO 10188 --- [           main] e.camel.management.JmxManagementStrategy : JMX is enabled
2022-03-10 14:44:37.430  INFO 10188 --- [           main] org.apache.camel.main.DownloaderHelper   : Downloaded dependency: org.apache.camel:camel-gson:3.15.0 took: 500ms
2022-03-10 14:44:37.535  INFO 10188 --- [           main] org.apache.camel.main.DownloaderHelper   : Downloaded dependency: org.apache.camel:camel-slack:3.15.0 took: 105ms
2022-03-10 14:44:38.853  INFO 10188 --- [           main] e.camel.impl.engine.AbstractCamelContext : Routes startup (total:3 started:3)
2022-03-10 14:44:38.853  INFO 10188 --- [           main] e.camel.impl.engine.AbstractCamelContext :     Started route1 (kamelet://slack-source)
2022-03-10 14:44:38.853  INFO 10188 --- [           main] e.camel.impl.engine.AbstractCamelContext :     Started slack-source-1 (slack://general)
2022-03-10 14:44:38.853  INFO 10188 --- [           main] e.camel.impl.engine.AbstractCamelContext :     Started log-sink-2 (kamelet://source)
2022-03-10 14:44:38.854  INFO 10188 --- [           main] e.camel.impl.engine.AbstractCamelContext : Apache Camel 3.15.0 (CamelJBang) started in 2s152ms (build:123ms init:804ms start:1s225ms)
2022-03-10 14:44:38.854  INFO 10188 --- [           main] ache.camel.impl.debugger.BacklogDebugger : Enabling debugger
2022-03-10 14:44:40.105  INFO 10188 --- [slack://general] info                                     : Exchange[ExchangePattern: InOnly, Headers: {Content-Type=application/json}, BodyType: byte[], Body: {"type":"message","team":"xxxx","user":"yyyy","text":"hello","blocks":[{"type":"rich_text","elements":[{"type":"rich_text_section","elements":[{"type":"text","text":"hello"}]}],"blockId":"XAE5"}],"ts":"1646919166.690039","is_intro":false,"is_starred":false,"wibblr":false,"displayAsBot":false,"upload":false,"clientMsgId":"4da336d2-fafe-4442-b307-d3ae2961ba3a","unfurlLinks":false,"unfurlMedia":false,"is_thread_broadcast":false,"is_locked":false,"subscribed":false,"hidden":false}]
^C2022-03-10 14:44:47.276  INFO 10188 --- [           main] e.camel.impl.engine.AbstractCamelContext : Apache Camel 3.15.0 (CamelJBang) shutting down (timeout:5s)
2022-03-10 14:44:47.285  INFO 10188 --- [           main] e.camel.impl.engine.AbstractCamelContext : Routes stopped (total:3 stopped:3)
2022-03-10 14:44:47.285  INFO 10188 --- [           main] e.camel.impl.engine.AbstractCamelContext :     Stopped log-sink-2 (kamelet://source)
2022-03-10 14:44:47.285  INFO 10188 --- [           main] e.camel.impl.engine.AbstractCamelContext :     Stopped slack-source-1 (slack://general)
2022-03-10 14:44:47.285  INFO 10188 --- [           main] e.camel.impl.engine.AbstractCamelContext :     Stopped route1 (kamelet://slack-source)
2022-03-10 14:44:47.286  INFO 10188 --- [           main] ache.camel.impl.debugger.BacklogDebugger : Disabling debugger
2022-03-10 14:44:47.288  INFO 10188 --- [           main] e.camel.impl.engine.AbstractCamelContext : Apache Camel 3.15.0 (CamelJBang) shutdown in 12ms (uptime:9s659ms)
```
