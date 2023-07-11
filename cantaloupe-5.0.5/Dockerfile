FROM ubuntu

COPY cantaloupe-5.0.5.jar cantaloupe-5.0.5.jar
COPY cantaloupe.properties cantaloupe.properties
COPY KeyStore.jks KeyStore.jks

EXPOSE 8182

RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive \
    apt-get -y install default-jre-headless && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* 

CMD java -Dcantaloupe.config=./cantaloupe.properties -Xmx2g -jar cantaloupe-5.0.5.jar