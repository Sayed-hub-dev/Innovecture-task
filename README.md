# Hello-World !
## This repository consits of a hello-world application. it shows

## 1.Run & test the application from cli
## 2.Create a docker image, run the        container and test it.

# Create a sample html file
> index.html
## inside a  .html will have a code hello-world
# Creating a Dockerfile
## by writing the dockerfile we can install webserver apache and deploy the application
> FROM httpd:2.4
COPY index.html /usr/local/apache2/htdocs/
# Create a docker-compose file
> version: '2'
  services:
    apache:
      build: .
      image: "httpd:2.4"
      ports:
        - '80:80'
# Install docker 
##   Here we are going to install docker to create, deploy and run applications by using containers.
# Install docker-compose
##   Here we are installing docker-compose for defining and running multi-container, With Compose, we can  use a YAML file to configure our application's services.
## By using below command we can build,run,test our Application
> docker-compose up
## Test our application
## by using below command we can test our application  
> http://localhost:80
