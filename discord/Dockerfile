FROM golang:1.8

WORKDIR /project

COPY /cmd /usr/local/go/src/cmd 
COPY /vendor /usr/local/go/src/vendor
COPY /cmd/bot/audio /project/audio

RUN go install cmd/bot
RUN cp /usr/local/go/bin/bot /project/bot

CMD /project/bot -t DISCORD_TOKEN