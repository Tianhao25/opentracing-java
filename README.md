# Experiment with Open-tracing

## What is OpenTracing
To me, opentracing is a standard that can be implemented by different vendors to provide distributed application tracing function. The meaning of standard is that it must run with some OPT implementations such as Jaeger(by Uber). 

[link to Jaeger](http://jaeger.readthedocs.io/en/latest/)

## Get started with Jaeger
Install dokcer here:  
https://www.docker.com/community-edition#/download  

Verify your installation with:  
```bash
docker info
```
Start Jaeger with Docker
```bash
docker run -d -e COLLECTOR_ZIPKIN_HTTP_PORT=9411 -p5775:5775/udp -p6831:6831/udp -p6832:6832/udp \
  -p5778:5778 -p16686:16686 -p14268:14268 -p9411:9411 jaegertracing/all-in-one:latest
```

**Now you have a Jaeger server started at 16686 port, [take a look](http://localhost:16686/search)**  
With this Jaeger server, we can then do some improvement in our project to allow tracing in Jaeger.

