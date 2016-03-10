# HiddenDocker
A Tor Hidden Service Proxy in Docker

## What is this?
This is a Docker Image that launches `tor(1)` inside a Docker Container and configures it to run a single Hidden Service on port `tcp/80` from which all traffic is forwarded to a linked container, again on port `tcp/80`. 

## How to run this?

You can run this locally:

```bash
docker build .
docker run -d --link <HiddenService>:hidden.service <ImageID>
```

or directly from Docker Hub:

```bash
docker run -d --link <HiddenService>:hidden.service daknob/hiddendocker
```
