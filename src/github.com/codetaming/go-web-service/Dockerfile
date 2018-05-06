FROM alexellis2/go-armhf:1.7.4
RUN mkdir /app
ADD . /app/
WORKDIR /app
RUN go build -o main .
CMD ["/app/main"]
EXPOSE 8080