# Use eclipse-temurin:16-jdk instead of Zulu to avoid this error when building for ARM64: 
# ERROR: failed to build: ... /bin/sh: Invalid ELF image for this architecture

FROM eclipse-temurin:16-jdk 

RUN apt-get update && apt-get install -y curl wget && rm -rf /var/lib/apt/lists/*

WORKDIR /app/data

CMD ["sh", "-c", "trap 'kill -TERM $child 2>/dev/null; wait $child' TERM INT; exec $START & child=$!; wait $child"]