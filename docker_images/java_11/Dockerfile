FROM eclipse-temurin:11-jdk-alpine

RUN apk update && \
    apk upgrade && \
    apk add --no-cache sqlite-libs>=3.48.0-r3 && \
    rm -rf /var/cache/apk/*
    
WORKDIR /app/data

CMD ["sh", "-c", "trap 'exit 0' TERM INT; exec $START"]