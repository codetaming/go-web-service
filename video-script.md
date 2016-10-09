I wanted to take a minute to make a short video showing how straight forward it is to create a simple web service in Go and publish it on DockerHub.

Here in IntelliJ I have created a new project with a Go file named main.go.

- My package is main
- I have imported the fmt and net/http packages from the standard library.

Here I have created a handler that takes a request and returns a string with the first path variable from the URL included.

I have defined a main method assigning my handler to  requests on the root URL and finally created a HTTP server on port 8080.

I can run that now, go to my browser and it is working.

To make this into a Docker image I have a very minimal Dockerfile.
 
It uses the default Go image and use the onbuild trigger which will copy the executable, run go get and go install. Then on the second line I am exposing 8080, the port which the server is running on.

I build the docker image

```
docker build -t codetaming/go-web-service .
```

and run it

```
docker run --publish 8080:8080 -t codetaming/go-web-service
```

If I test it in my browser again, there it is.

Now I can login to Docker hub and publish it. As simple as that.

```
docker login
docker push codetaming/go-web-service
```




