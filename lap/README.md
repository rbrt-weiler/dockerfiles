# lap

A Dockerfile that creates a web server environment, useful for testing websites.

## Contents

The Dockerfile is based on the official PHP repository and uses PHP 7.2. It adds a few PHP modules that I required for testing purposes at some point.

## Usage

* Build an actual Docker image from the Dockerfile:  
  `cd` into the directory where the Dockerfile is located and `docker build --compress --pull -t lap .`
* Use the image to start a container:  
  `docker run -d -p 8000:80 --name lap-container -v /path/to/website:/var/www/html lap`  
  You should be able to access your website using http://localhost:8000/ now.
* Stop and delete the container:  
  `docker stop lap-container && docker rm lap-container`
