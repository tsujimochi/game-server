FROM openjdk:23-slim

ARG DOWNLOAD_LINK

RUN apt update && apt install -y wget
RUN mkdir -p /var/games/ && cd /var/games/ && wget -O server.jar ${DOWNLOAD_LINK}
RUN echo "eula=true" > /var/games/eula.txt

CMD cd /var/games/ && java -Xmx1024M -Xms1024M -jar /var/games/server.jar nogui
