FROM arm32v7/golang AS build-env
WORKDIR /app
ADD . /app/
RUN cd /app && go build -o goapp

FROM arm32v7/golang
RUN apk update && apk add ca- certificates && rm -rf /var/cache/apk/*
WORKDIR /app
COPY --from=build-env /app/goapp /app

EXPOSE 8080
ENTRYPOINT ./goapp