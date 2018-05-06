## Synopsis

A very simple Go Web Service.

A video of the process of creating the service and Docker image can be seen on [YouTube](https://youtu.be/-IoWzON4IRA)

## Run
```
go run main.go
```

## Build
```
go build
```

## Run Go Executable
```
./go-web-service
```

## Build Docker

```
docker build -t codetaming/go-web-service-arm .
```

## Run Docker
```
docker run --publish 8080:8080 -t codetaming/go-web-service-arm
```

## Push to Docker Hub
```
docker login
docker push codetaming/go-web-service-arm
```

## Test in Browser
[http://localhost:8080/Code%20Taming](http://localhost:8080/Code%20Taming)