FROM node:22-bookworm-slim

# testinng patch cve
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y --only-upgrade \
        zlib1g \
        perl-base \
        ncurses-bin \
        ncurses-base \
        libtinfo6 \
        libpam-modules-bin \
        libpam-runtime \
        libpam0g \
        libpam-modules \
        coreutils \
        libapt-pkg6.0 \
        apt \
        gpgv \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app/data

CMD ["sh", "-c", "trap 'exit 0' TERM INT; exec $START"]