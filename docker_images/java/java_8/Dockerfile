FROM eclipse-temurin:8-jdk-alpine

RUN apk update && \
    apk upgrade && \
    apk add --no-cache \
        sqlite-libs>=3.48.0-r3 \
        curl \
        wget \
        && rm -rf /var/cache/apk/*

WORKDIR /app/data

CMD ["sh", "-c", "trap 'kill -TERM $child 2>/dev/null; wait $child' TERM INT; exec $START & child=$!; wait $child"]