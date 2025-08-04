FROM alpine:latest

WORKDIR /app

# Unduh binary PocketBase dari release resmi
ADD https://github.com/pocketbase/pocketbase/releases/download/v0.22.11/pocketbase_0.22.11_linux_amd64.zip .

# Unzip binary
RUN apk add --no-cache unzip && \
    unzip pocketbase_0.22.11_linux_amd64.zip && \
    chmod +x pocketbase && \
    rm pocketbase_0.22.11_linux_amd64.zip

# Tambahkan folder untuk data
COPY pb_data ./pb_data

EXPOSE 8090

CMD ["./pocketbase", "serve", "--http=0.0.0.0:8090"]
