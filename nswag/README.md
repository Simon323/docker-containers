## Run docker compose
```bash
docker-compose -f docker-compose.yml up
```
OR
```bash
docker-compose -f docker-compose.yml up -d
```

## Build container 
```bash
docker build -f Dockerfile.dev -t my-node-nswag-container .
```

## Run and enter to container
```bash
docker run -it -p 5750:8080 my-node-nswag-container
```

### Generate nswag c# class
```bash
nswag openapi2csclient /input:openapi.yaml /classname:GeneratedApiClient /namespace:ApiGateway
```