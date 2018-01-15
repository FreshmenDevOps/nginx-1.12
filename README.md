## nginx-1.12 + Google Pagespeed

[NGINX](http://nginx.org/) bundle with support for Google Pagespeed [ngx_pagespeed](https://github.com/pagespeed/ngx_pagespeed)

### Base Docker Image

* [centos7](http://dockerfile.github.io/#/centos)


### Installation

1. Install [Docker](https://www.docker.com/).

2. Clone this repo

3. Build an image from Dockerfile: `docker build -t="nginx:1.12" -f="nginx-1.12/Dockerfile"`)


### Usage

    docker run -d -p 80:8180 -p 443:8543

#### Attach persistent/shared directories

    docker run -d -p 80:8180 -p 443:8543 -v <nginx-dir>:/etc/nginx:ro -v <log-dir>:/var/log/nginx -v <html-dir>:/srv/www nginx:1.12

Open `http://<host>:8180` to verify.

