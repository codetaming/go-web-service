FROM arm32v7/golang AS build-env
WORKDIR /app
ADD . /app/
RUN cd /app && go build -o goapp .

FROM armhf/alpine
RUN apk update && apk add ca-certificates && rm -rf /var/cache/apk/*
WORKDIR /app
COPY --from=build-env /app/goapp .

EXPOSE 8080
ENTRYPOINT ./app/goapp