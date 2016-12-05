# OctoPrint Virtual printer
Sometimes you need to test your OctoPrint plugin, API client or whatever you are building with virtual printer. This docker image contains clean install of OctoPrint 1.2.13. *On first run* you will be asked for new password.

# Usage

Depends on your needs, you can build image yourself or use prebuilt. Prebuilt image is automated build. In both cases, demonstrated use cases runs on port `3200`.

## Build it

This repository contains Dockerfile which allows you to build image on your own with following command:

```
docker build -t virtuprint .
```

This builds new image named `virtuprint`. To create new container from this image, run:

```
docker run --rm --name myoctoprint -p3200:5000 virtuprint
```

Docker creted new container

## Prebuilt

If you are not interested in modifing Dockerfile or just more comfortable with pulling image, you can simply run:

```
docker run --rm --name myoctoprint -p3200:5000 josefdolezal/virtuprint
```

# License
The VirtuPrint Dockerfile is licensed under [MIT](LICENSE).
