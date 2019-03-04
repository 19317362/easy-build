build-aosp
==========

Modified from [gmacario/build-aosp](https://github.com/gmacario/easy-build)

This project helps rebuilding firmware images of the [Android Open Source Project](http://source.android.com/source/index.html).

WARNING: Still experimental, use at your own risk!

### Build the Docker image

```
$ docker build -t <your tag> .
```

### Using the Docker image to build your AOSP

```BASH
$ cd ~/aosp
$ docker run -ti --rm -v $PWD:/home/build:rw <your tag> bash
```

Then logged as build@container:

```
$ source ./build/envsetup.sh
$ lunch <your prj>
$ make -j8
```

<!-- EOF -->
