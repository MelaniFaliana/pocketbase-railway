FROM alpine:latest

RUN apk add --no-cache curl

WORKDIR /app

# Ganti URL di bawah ini dengan URL dari GitHub release kamu
RUN curl -L -o pocketbase https://github.com/username/nama-repo/releases/download/v1/pocketbase \
    && chmod +x pocketbase

EXPOSE 8090
ENTRYPOINT ["./pocketbase", "serve", "--http=0.0.0.0:8090"]
