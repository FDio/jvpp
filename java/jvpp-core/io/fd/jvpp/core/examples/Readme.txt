This package contains basic examples for jvpp. To run the examples:

- Make sure VPP is running
- From VPP's build-root/ folder execute:
  - release version: sudo java -cp build-vpp-native/vpp/vpp-api/java/jvpp-registry-18.01.jar:build-vpp-native/vpp/vpp-api/java/jvpp-core-18.01.jar io.fd.jvpp.core.examples.[test name]
  - debug version: sudo java -cp build-vpp_debug-native/vpp/vpp-api/java/jvpp-registry-18.01.jar:build-vpp_debug-native/vpp/vpp-api/java/jvpp-core-18.01.jar io.fd.jvpp.core.examples.[test name]

Available examples:
CallbackApiExample - Similar to ControlPingTest, invokes more complex calls (e.g. interface dump) using low level JVpp APIs
CallbackJVppFacadeNotificationExample - Example of interface notifications using Callback based JVpp facade
CallbackJVppFacadeExample - Execution of more complex calls using Callback based JVpp facade
CallbackNotificationApiExample -  Example of interface notifications using low level JVpp APIs
CreateSubInterfaceExample - Example of sub-interface creation
FutureApiNotificationExample - Example of interface notifications using Future based JVpp facade
FutureApiExample - Execution of more complex calls using Future based JVpp facade
L2AclExample - Example of L2 ACL creation
LispAdjacencyExample - Example of lisp adjacency creation and read (custom vpe.api type support showcase)

CallbackApiReadPerfTest, FutureApiReadPerfTest, CallbackApiWritePerfTest - test provide two ways to count invocations:
1) maximum number of invocations and received replyies within 1 sec
sudo java -cp build-vpp-native/vpp/vpp-api/java/jvpp-registry-18.01.jar:build-vpp-native/vpp/vpp-api/java/jvpp-core-18.01.jar io.fd.jvpp.core.examples.[test name]
2) measure time in ns from first request to receiving last reply over set amount of requests
sudo java -cp build-vpp-native/vpp/vpp-api/java/jvpp-registry-18.01.jar:build-vpp-native/vpp/vpp-api/java/jvpp-core-18.01.jar io.fd.jvpp.core.examples.[test name] [number of request to send]

