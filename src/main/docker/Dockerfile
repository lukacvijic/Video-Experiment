FROM linuxserver/ffmpeg:6.1.1

ENV JAVA_HOME=/opt/java/openjdk

COPY --from=eclipse-temurin:21 $JAVA_HOME $JAVA_HOME

ENV PATH="${JAVA_HOME}/bin:${PATH}"

WORKDIR /opt/applications/streaming

COPY target/*-runner.jar ./streaming.jar

EXPOSE 8080

ENTRYPOINT [ "java",  "-jar", "streaming.jar" ]

