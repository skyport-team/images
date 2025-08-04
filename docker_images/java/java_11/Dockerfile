FROM azul/zulu-openjdk:11

RUN apt-get update && apt-get install -y curl wget && rm -rf /var/lib/apt/lists/*

WORKDIR /app/data

CMD ["sh", "-c", "trap 'kill -TERM $child 2>/dev/null; wait $child' TERM INT; exec $START & child=$!; wait $child"]