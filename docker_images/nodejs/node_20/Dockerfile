FROM node:20-bookworm-slim 

RUN apt-get update && \
    apt-get upgrade -y && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /app/data

CMD ["sh", "-c", "trap 'exit 0' TERM INT; exec $START"]