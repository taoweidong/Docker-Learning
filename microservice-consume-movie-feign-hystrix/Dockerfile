FROM java:8
VOLUME /tmp
ADD /target/microservice-consume-movie-feign-hystrix-1.0-SNAPSHOT.jar app.jar
RUN bash -c 'touch /app.jar'
EXPOSE 9103
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]