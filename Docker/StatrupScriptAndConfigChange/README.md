# Docker > Startup Script & Config Change

## Outline 

This snippet is an example of creating a docker container that has some default values embedded that we want to overwrite with some envionment varibales. 

## Use Case

I created this snippet to test the ability to run angular in dcoker and build a single image. THis is not possible using the angular envionment configuration mechansim as you'd need a different docker image for each envionment. 

The root of the problem was that in one way or the other I need to configure the container to contact the correct instance of the api and therefore at runtime I need to specify this. 

On migrating the project to codespaces then the API is not acceible on localhost. Nor is it accesible on host.docker.internal so we need to be able to build and specify the API location for the angular client at runtime. 