# Experiment with Open-tracing

## Get started
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


