# Lagom in Action


# Dependency tree of a basic Lagom project

```
+- com.lightbend.lagom:lagom-javadsl-api_2.12:jar:1.4.6:compile
| +- org.scala-lang:scala-library:jar:2.12.6:compile
| +- com.lightbend.lagom:lagom-api_2.12:jar:1.4.6:compile
| | +- org.scala-lang.modules:scala-parser-combinators_2.12:jar:1.0.4:compile
| | +- org.scala-lang.modules:scala-xml_2.12:jar:1.0.6:compile
| | +- com.typesafe.akka:akka-actor_2.12:jar:2.5.13:compile
| | | \- com.typesafe:config:jar:1.3.2:compile
| | +- com.typesafe.akka:akka-slf4j_2.12:jar:2.5.13:compile
| | +- com.typesafe.akka:akka-stream_2.12:jar:2.5.13:compile
| | | +- com.typesafe.akka:akka-protobuf_2.12:jar:2.5.13:compile
| | | +- org.reactivestreams:reactive-streams:jar:1.0.2:compile
| | | \- com.typesafe:ssl-config-core_2.12:jar:0.2.3:compile
| | +- com.typesafe.play:play_2.12:jar:2.6.13:compile
| | | +- com.typesafe.play:build-link:jar:2.6.13:compile
| | | | \- com.typesafe.play:play-exceptions:jar:2.6.13:compile
| | | +- com.typesafe.play:play-netty-utils:jar:2.6.13:compile
| | | +- com.typesafe.play:play-streams_2.12:jar:2.6.13:compile
| | | +- com.typesafe.play:twirl-api_2.12:jar:1.3.14:compile
| | | +- com.fasterxml.jackson.core:jackson-core:jar:2.8.11:compile
| | | +- com.fasterxml.jackson.core:jackson-annotations:jar:2.8.11:compile
| | | +- com.fasterxml.jackson.core:jackson-databind:jar:2.8.11:compile
| | | +- com.fasterxml.jackson.datatype:jackson-datatype-jdk8:jar:2.8.11:compile
| | | +- com.fasterxml.jackson.datatype:jackson-datatype-jsr310:jar:2.8.11:compile
| | | +- commons-codec:commons-codec:jar:1.10:compile
| | | +- io.jsonwebtoken:jjwt:jar:0.7.0:compile
| | | +- org.apache.commons:commons-lang3:jar:3.6:compile
| | | +- javax.transaction:jta:jar:1.1:compile
| | | +- javax.inject:javax.inject:jar:1:compile
| | | \- org.scala-lang:scala-reflect:jar:2.12.4:compile
| | +- com.google.guava:guava:jar:22.0:compile
| | | +- com.google.code.findbugs:jsr305:jar:1.3.9:compile
| | | +- com.google.errorprone:error_prone_annotations:jar:2.0.18:compile
| | | +- com.google.j2objc:j2objc-annotations:jar:1.1:compile
| | | \- org.codehaus.mojo:animal-sniffer-annotations:jar:1.14:compile
| | \- com.typesafe.play:play-json_2.12:jar:2.6.9:compile
| | +- com.typesafe.play:play-functional_2.12:jar:2.6.9:compile
| | +- org.typelevel:macro-compat_2.12:jar:1.1.1:compile
| | \- joda-time:joda-time:jar:2.9.9:compile
| +- com.typesafe.play:play-java_2.12:jar:2.6.13:compile
| | +- org.scala-lang.modules:scala-java8-compat_2.12:jar:0.8.0:compile
| | +- org.reflections:reflections:jar:0.9.11:compile
| | \- net.jodah:typetools:jar:0.5.0:compile
| +- com.typesafe.play:play-guice_2.12:jar:2.6.13:compile
| | +- com.google.inject:guice:jar:4.1.0:compile
| | | \- aopalliance:aopalliance:jar:1.0:compile
| | \- com.google.inject.extensions:guice-assistedinject:jar:4.1.0:compile
| \- org.pcollections:pcollections:jar:2.1.2:compile
+- com.lightbend.lagom:lagom-javadsl-kafka-broker_2.12:jar:1.4.6:compile
| +- com.lightbend.lagom:lagom-javadsl-broker_2.12:jar:1.4.6:compile
| | \- com.lightbend.lagom:lagom-javadsl-persistence_2.12:jar:1.4.6:compile
| | +- com.lightbend.lagom:lagom-javadsl-cluster_2.12:jar:1.4.6:compile
| | \- com.typesafe.akka:akka-testkit_2.12:jar:2.5.13:compile
| +- com.lightbend.lagom:lagom-kafka-broker_2.12:jar:1.4.6:compile
| | +- com.lightbend.lagom:lagom-persistence-core_2.12:jar:1.4.6:compile
| | | +- com.lightbend.lagom:lagom-cluster-core_2.12:jar:1.4.6:compile
| | | | \- com.typesafe.akka:akka-cluster_2.12:jar:2.5.13:compile
| | | | \- com.typesafe.akka:akka-remote_2.12:jar:2.5.13:compile
| | | | +- io.netty:netty:jar:3.10.6.Final:compile
| | | | +- io.aeron:aeron-driver:jar:1.9.1:compile
| | | | \- io.aeron:aeron-client:jar:1.9.1:compile
| | | | \- org.agrona:agrona:jar:0.9.17:compile
| | | +- com.typesafe.akka:akka-persistence_2.12:jar:2.5.13:compile
| | | +- com.typesafe.akka:akka-persistence-query_2.12:jar:2.5.13:compile
| | | \- com.typesafe.akka:akka-cluster-sharding_2.12:jar:2.5.13:compile
| | | +- com.typesafe.akka:akka-distributed-data_2.12:jar:2.5.13:compile
| | | | \- org.lmdbjava:lmdbjava:jar:0.6.0:compile
| | | | +- com.github.jnr:jnr-ffi:jar:2.1.6:compile
| | | | | +- com.github.jnr:jffi:jar:1.2.16:compile
| | | | | +- com.github.jnr:jffi:jar:native:1.2.16:runtime
| | | | | +- org.ow2.asm:asm:jar:5.0.3:compile
| | | | | +- org.ow2.asm:asm-commons:jar:5.0.3:compile
| | | | | +- org.ow2.asm:asm-analysis:jar:5.0.3:compile
| | | | | +- org.ow2.asm:asm-tree:jar:5.0.3:compile
| | | | | +- org.ow2.asm:asm-util:jar:5.0.3:compile
| | | | | \- com.github.jnr:jnr-x86asm:jar:1.0.2:compile
| | | | \- com.github.jnr:jnr-constants:jar:0.9.9:compile
| | | \- com.typesafe.akka:akka-cluster-tools_2.12:jar:2.5.13:compile
| | \- com.lightbend.lagom:lagom-kafka-client_2.12:jar:1.4.6:compile
| | +- org.slf4j:log4j-over-slf4j:jar:1.7.25:compile
| | \- com.typesafe.akka:akka-stream-kafka_2.12:jar:0.18:compile
| +- com.lightbend.lagom:lagom-javadsl-kafka-client_2.12:jar:1.4.6:compile
| +- com.lightbend.lagom:lagom-javadsl-server_2.12:jar:1.4.6:compile
| | +- com.lightbend.lagom:lagom-server_2.12:jar:1.4.6:compile
| | | \- com.lightbend.lagom:lagom-client_2.12:jar:1.4.6:compile
| | | +- com.lightbend.lagom:lagom-spi_2.12:jar:1.4.6:compile
| | | +- com.typesafe.play:play-ws_2.12:jar:2.6.13:compile
| | | | +- com.typesafe.play:play-ws-standalone_2.12:jar:1.1.7:compile
| | | | +- com.typesafe.play:play-ws-standalone-xml_2.12:jar:1.1.7:compile
| | | | \- com.typesafe.play:play-ws-standalone-json_2.12:jar:1.1.7:compile
| | | +- com.typesafe.play:play-ahc-ws_2.12:jar:2.6.13:compile
| | | | +- com.typesafe.play:play-ahc-ws-standalone_2.12:jar:1.1.7:compile
| | | | | \- com.typesafe.play:cachecontrol_2.12:jar:1.1.2:compile
| | | | | \- org.joda:joda-convert:jar:1.7:compile
| | | | +- com.typesafe.play:shaded-asynchttpclient:jar:1.1.7:compile
| | | | +- com.typesafe.play:shaded-oauth:jar:1.1.7:compile
| | | | \- javax.cache:cache-api:jar:1.0.0:compile
| | | +- io.dropwizard.metrics:metrics-core:jar:3.2.2:compile
| | | +- com.typesafe.netty:netty-reactive-streams:jar:2.0.0:compile
| | | +- io.netty:netty-codec-http:jar:4.1.23.Final:compile
| | | | \- io.netty:netty-codec:jar:4.1.23.Final:compile
| | | \- io.netty:netty-handler:jar:4.1.23.Final:compile
| | | +- io.netty:netty-buffer:jar:4.1.23.Final:compile
| | | | \- io.netty:netty-common:jar:4.1.23.Final:compile
| | | \- io.netty:netty-transport:jar:4.1.23.Final:compile
| | | \- io.netty:netty-resolver:jar:4.1.23.Final:compile
| | +- com.lightbend.lagom:lagom-javadsl-client_2.12:jar:1.4.6:compile
| | \- com.lightbend.lagom:lagom-javadsl-jackson_2.12:jar:1.4.6:compile
| | +- com.fasterxml.jackson.module:jackson-module-parameter-names:jar:2.8.11:compile
| | +- com.fasterxml.jackson.datatype:jackson-datatype-pcollections:jar:2.8.11:compile
| | \- com.fasterxml.jackson.datatype:jackson-datatype-guava:jar:2.8.11:compile
| +- com.lightbend.lagom:lagom-kafka-server_2.12:jar:1.4.6:compile
| | +- org.apache.kafka:kafka_2.12:jar:0.11.0.1:compile
| | | +- org.apache.kafka:kafka-clients:jar:0.11.0.1:compile
| | | | +- net.jpountz.lz4:lz4:jar:1.3.0:compile
| | | | \- org.xerial.snappy:snappy-java:jar:1.1.2.6:compile
| | | +- net.sf.jopt-simple:jopt-simple:jar:5.0.3:compile
| | | +- com.yammer.metrics:metrics-core:jar:2.2.0:compile
| | | +- com.101tec:zkclient:jar:0.10:compile
| | | \- org.apache.zookeeper:zookeeper:jar:3.4.10:compile
| | +- org.apache.curator:curator-framework:jar:2.10.0:compile
| | | \- org.apache.curator:curator-client:jar:2.10.0:compile
| | +- org.apache.curator:curator-test:jar:2.10.0:compile
| | | \- org.apache.commons:commons-math:jar:2.2:compile
| | \- org.javassist:javassist:jar:3.21.0-GA:compile
| +- com.lightbend.lagom:lagom-kafka-server_2.12:pom:1.4.6:compile
| +- org.slf4j:slf4j-api:jar:1.7.25:compile
| \- log4j:log4j:jar:1.2.17:compile
\- org.projectlombok:lombok:jar:1.16.10:compile
```