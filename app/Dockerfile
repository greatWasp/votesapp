FROM debian
FROM maven

RUN apt-get update && apt-get install -y git
RUN git clone https://github.com/greatWasp/votesapp
RUN cd /votesapp/src/main/resources && \
    cp ./application.properties.sample ./application.properties && \
    sed -i 's/localhost:3306/db:3306/' ./application.properties
CMD cd /votesapp && mvn spring-boot:run
