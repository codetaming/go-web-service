## Synopsis

A very simple Go Web Service.

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
docker build -t codetaming/go-web-service .
```

## Run Docker
```
docker run --publish 8080:8080 -t codetaming/go-web-service
```

## Push to Docker Hub
```
docker login
docker push codetaming/go-web-service
```

## Test in Browser
[http://localhost:8080/Code%20Taming](http://localhost:8080/Code%20Taming)