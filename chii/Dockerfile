FROM node:14

WORKDIR /app

COPY ./app /app

ENV CHII_DOMAIN=example.doamin.app

CMD npx chii start -p 2444 -d $CHII_DOMAIN
# CMD ["sh", "-c", "npx chii start -p 2444 -d $CHII_DOMAIN"]
