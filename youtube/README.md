# download youtube and other videos

## Why not directly install?

Any python package comes with lots of dependencies. Maintaining them across differ applications is hard. Although we have a pyenv kind of version management tool, for each application the dependency may vary with the version of the library. 

Also keep your system clean, when you want to use the tool it starts and then it dies. Only the docker image occupies a bit of space. That can be always cleared using 

docker image prune -a

## Information

We are downloading the videos in the current directory which is map to docker volume /media.

This image is for ARM64 format of instruction (Mac M1)

## How to run

1. compile the docker image

```
docker build -t youtube-dl .
```

2. run the instance to download video and stop the instance after run

```
docker run --rm -v $(pwd):/media youtube-dl URL_TO_DOWNLOAD
```

