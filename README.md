# Creating a golang Docker image for use on OpenMind

The [Dockerfile](/Dockerfile) in this repository is used to build a Docker image. I created [a repository on DockerHub](https://hub.docker.com/r/kaczmarj/docker-golang-example/) that automatically builds a Docker image according to the Dockerfile in this GitHub repository. That Docker image can be pulled as a Singularity image onto OpenMind.


## Building the image yourself

(requires [Docker](https://www.docker.com/community-edition))

Clone this repository and build an image using the repo's Dockerfile.

```shell
$> git clone https://github.com/kaczmarj/docker-golang-example.git
$> cd docker-golang-example
$> docker build -t image-name-here .
$> docker images  # You will see 'image-name-here' listed as an image.
```


## Getting the Docker image onto OpenMind as a Singularity image

```shell
$> module add openmind/singularity/2.3
$> singularity pull docker://kaczmarj/docker-golang-example
```


## Getting the Docker image onto your own computer

(requires [Docker](https://www.docker.com/community-edition))

```shell
$> docker pull kaczmarj/docker-golang-example
```
