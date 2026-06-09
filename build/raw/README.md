## Building raw fs with docker

### Build Example

```cmd
docker build -t uxdroid-raw-builder .
docker run --privileged --name uxdroid-raw -i -t uxdroid-raw-builder
docker cp uxdroid-raw:/root/ux-cook/out/hirsute-raw-arm64.tar.gz .
docker cp uxdroid-raw:/root/ux-cook/out/hirsute-raw-armhf.tar.gz .
docker cp uxdroid-raw:/root/ux-cook/out/hirsute-raw-amd64.tar.gz .
```