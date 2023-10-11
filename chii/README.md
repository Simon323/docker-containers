## Build container
```bash
docker build -t chii:latest .
```

## Run container
```bash
docker run -d -p 2444:2444 --name chii chii:latest
```
Where:
- `-d` it's mean that the container will be running in background
- `-p 2444:2444` redirect container port to localhost:2444 
- `--name chii` it's container name
- `chii:latest` is version number of container image

## Docker compose
```bash
docker-compose up
```

## Run with parameter linux/unix
```bash
export CHII_DOMAIN=overrated.domain.app
docker-compose up
```

## Run with parameter windows
```bash
set CHII_DOMAIN=overrated.domain.app
docker-compose up
```