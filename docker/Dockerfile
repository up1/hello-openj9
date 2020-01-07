FROM adoptopenjdk:11-jre-openj9
RUN mkdir /opt/shareclasses
RUN mkdir /opt/app
COPY demo.jar /opt/app
CMD ["java", "-Xmx128m", "-XX:+IdleTuningGcOnIdle", "-Xtune:virtualized", "-Xscmx128m", "-Xscmaxaot100m", "-Xshareclasses:cacheDir=/opt/shareclasses", "-jar", "/opt/app/demo.jar"]