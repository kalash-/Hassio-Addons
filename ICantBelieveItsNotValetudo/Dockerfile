ARG BUILD_FROM
FROM $BUILD_FROM AS BUILD

ENV LANG C.UTF-8
ENV ICANTBELIEVEITSNOTVALETUDO_VERSION master

RUN apk add --no-cache git=2.20.1-r0 npm=10.14.2-r0
RUN git clone https://github.com/Hypfer/ICantBelieveItsNotValetudo.git -b $ICANTBELIEVEITSNOTVALETUDO_VERSION /app

WORKDIR /app
RUN npm install

COPY run.sh /
RUN chmod a+x /run.sh
CMD [ "/run.sh" ]
