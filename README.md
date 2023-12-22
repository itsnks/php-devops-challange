# intuji-devops-internship-challenge


## 1. Installing Docker

to install docker run the following command:

```
./docker-install.sh
```

## Building and pushing docker image

### 2.1. Building Docker image

- php app was cloned using 
```
git clone https://github.com/silarhi/php-hello-world.git
```
<img src="img/clone.png">

- The `Dockerfile` uses `php:7.4-apache` as base image and runs based on instructions given in github repository above
- The `index.php` file is deployed using `apache2` as the web server
- To build the image run:
```
docker build -t nikeshhh/phpapp-intuji .
```
<img src="img/docker-build.png">
### 2.2. Pushing the image to Dockerhub

- To connect with dockerhub user:
```
docker login
```
- The image is pushed to dockerhub using
```
docker push nikeshhh/phpapp-intuji
```
<img src="img/docker-push.png">
## 3. Docker-compose file 

- Docker compose uses the image built in the previous step either locally available or pulls from dockerhub
- To run the compose file use

```
docker compose up
```

## 4. Jenkins

- Jenkins can be installed using either the [Docker container installation](https://hub.docker.com/r/jenkins/jenkins) or [Direct installation](https://pkg.jenkins.io/debian-stable/)
- Jenkins can be accessed in browser at 
```localhost:8080```
- After unlocking using initial password stored at `/var/lib/jenkins/secrets/initialAdminPassword` admin user is created
<img src="img/jenkins-user.png">
- On user creation, required extensions are installed
<img src="img/jenkins-extension.png">
- After the extensions have been installed you can head to jenkins home page
<img src="img/jenkins-home.png">
