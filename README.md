# docker-registry-proxy-example

This repo provide an example for docker pull through cache composed by two private registries

- Usage

```
// start the main and proxy registries by compose.
docker-compose up

// pull a hello world image.
docker pull hello-world

// re-tag the hello world image and push into main registry.
docker tag hello-world localhost:5000/hello-world
docker push localhost:5000/hello-world

// remove all your hello world images locally.
docker rmi hello-world localhost:5000/hello-world

// magic! now pull the image from proxy registry.
docker pull localhost:5005/hello-world
```
