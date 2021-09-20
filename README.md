# Atom
Atom editor in docker container

## Deploy the image 

To deploy already built and updated image you can run: 

```
docker run -d -v /tmp/.X11-unix/:/tmp/.X11-unix/ \
              -v /dev/shm:/dev/shm \
              -v ${HOME}/.atom:/home/atom/.atom \
              -e DISPLAY \
              melashri/atom
```

`-v /dev/shm:/dev/shm` is optional and you can replace it with `--shm-size="<number><unit>"`.

## Build Image

If you want instead to build the image locally you can run 

```
docker build . -t melashri/atom
```
