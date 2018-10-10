# udocker-build
Docker image to build udocker executable

The image is based in centos6 with python 3.4, and pyinstaller

## How to use this image

Pull the image from dockerhub

```
docker pull mariojmdavid/udocker-build
```

Clone the udocker repository, with whatever branch you want to build
this example uses a fork and specific branch:

```
git clone git@github.com:mariojmdavid/udocker.git -b devel3
```

Instantiate the container, mounting the github repository, and running
the pyinstaller to build a single executable of udocker

```
docker run -v $PWD/udocker:/home/udocker mariojmdavid/udocker-build pyinstaller -F -D udocker/udocker.py
```


