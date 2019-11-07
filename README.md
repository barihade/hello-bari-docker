# Hello Bari Docker
This is simple Hello World PHP Application deployed using Docker.

# How To Make It
1. First of all you'll need to install Docker if you haven't done that already. You can learn to install Docker at [Docker Official Documentation](https://docs.docker.com/install/).
2. Next, you need to build Docker image using Dockerfile. The Dockerfile contain information about parent image, project path inside the image, and exposed port. After creating Dockerfile inside the project directory, execute it using command : `docker build -t hello-bari .`
3. After that, you can run the container created using image "hello-bari" using command : `docker run -p 5000:80 hello-bari`
4. Or, you can create the container first using command : `docker container create --name app-hello -p 5000:80 hello-bari`. Then, you can run it using command : `docker container start app-hello`
5. You can access it, with typing `localhost:5000` on browser address bar.

# How It Works
Docker builds an image containing the application in src/ and all of its dependencies by using the Dockerfile contained in this repository.

The Dockerfile tells docker to use the [Official PHP Docker image](https://hub.docker.com/_/php) as the parent image.

The PHP image then uses the [Official Debian Jessie Docker image](https://hub.docker.com/_/debian) as its parent image.

At this point, an image has been built which contains Apache, PHP and all of the OS dependencies and libraries required to serve a webpage written in PHP.

Finally, docker copies everything in src/ inside this repository to the /var/www/html folder inside the image. This is the Apache web root directory.

# Setup
- Ensure you have Docker installed.
- `git clone` this repository.
- `docker build -t hello-bari .`
- `docker run -p 5000:80 hello-bari`

# Let's talk about some projects with me
Just Contact Me At :
- Email : barihade@gmail.com
- twitter : [@barihade](https://twitter.com/barihade)

# License
This repository is under [MIT](https://opensource.org/licenses/MIT) license.
