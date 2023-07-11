FROM ubuntu

WORKDIR /d2r
COPY . .


EXPOSE 2020

RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive \
    apt-get -y install default-jre-headless && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* 

CMD ./d2r-server mapping4.ttl