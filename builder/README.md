# Builder Abstract Image
This image is used as a base image for a builder container. You should extend it to build your application.
Don't forget to run this with `-v /var/run/docker.sock:/var/run/docker.sock` 

It contains:
- docker-ce 17.05
- docker-compose 1.13
- git

To build this image:
`docker-compose build`
