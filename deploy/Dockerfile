FROM alpine:latest

WORKDIR /app

# Unduh binary PocketBase dari rilis resmi
ADD https://github.com/pocketbase/pocketbase/releases/download/v0.22.11/pocketbase_0.22.11_linux_amd64.zip .

RUN apk add --no-cache unzip && \
    unzip pocketbase_0.22.11_linux_amd64.zip && \
    chmod +x pocketbase && \
    rm pocketbase_0.22.11_linux_amd64.zip

COPY pb_data ./pb_data

EXPOSE 8090

CMD ["./pocketbase", "serve", "--http=0.0.0.0:8090"]
