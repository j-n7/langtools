FROM openjdk:14-alpine

# see Makefile.version
ARG version

MAINTAINER Jan-Niklas Niebel <blogerboy98@gmail.com>

RUN apk add --no-cache libgomp gcompat libstdc++

RUN wget https://www.languagetool.org/download/LanguageTool-$version.zip && \
    unzip LanguageTool-$version.zip && \
    rm LanguageTool-$version.zip

WORKDIR /LanguageTool-$version

ADD start.sh /start.sh
CMD [ "sh", "/start.sh" ]

USER nobody
