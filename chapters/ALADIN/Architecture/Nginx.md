# NGINX

ALADIN uses NGINX:

- as a reverse proxy:
  - to serve the CARPET frontend,
  - the documentation and
  - provide file sharing.

## Setup

### Install NGINX

Utilize either the [official NGINX Docker image](https://hub.docker.com/_/nginx) or a bare metal installation - reference the [tutorial](https://www.nginx.com/resources/wiki/start/topics/tutorials/install/) required for your OS.

### Configure SSL

To setup SSL, follow the [tutorial](https://www.nginx.com/blog/using-free-ssltls-certificates-from-lets-encrypt-with-nginx/) provided by NGINX. The SSL-certificate is provided free of charfe by [Let's Encrypt](https://letsencrypt.org/). By utilizing certbot, the issued certificate can be renewed automatically.

### Final NGINX configuration

```
events {
  worker_connections  4096;  ## Default: 1024
}
http {
    server {
        root /var/www/html;
        server_name aladin.htw-dresden.de;

        listen [::]:443 ssl ipv6only=on; # managed by Certbot
        listen 443 ssl; # managed by Certbot
        ssl_certificate /etc/letsencrypt/live/aladin.htw-dresden.de/fullchain.pem; # managed by Certbot
        ssl_certificate_key /etc/letsencrypt/live/aladin.htw-dresden.de/privkey.pem; # managed by Certbot
        include /etc/letsencrypt/options-ssl-nginx.conf; # managed by Certbot
        ssl_dhparam /etc/letsencrypt/ssl-dhparams.pem; # managed by Certbot

        location /docs {
            proxy_pass https://htw-aladin.github.io/documentation;
        }
        location / {
            proxy_pass http://localhost:8000;
            proxy_http_version 1.1;
            proxy_set_header Upgrade $http_upgrade;
            proxy_set_header Connection 'upgrade';
            proxy_set_header Host $host;
            proxy_cache_bypass $http_upgrade;
        }
    }

    server {
        if ($host = aladin.htw-dresden.de) {
            return 301 https://$host$request_uri;
        } # managed by Certbot

        listen 80 default_server;
        listen [::]:80 default_server;

        server_name aladin.htw-dresden.de;
        return 404; # managed by Certbot
   }
}
```

### Test configuration

To test the NGINX configuration use the following commands (assuming a Linux environment):

#### Test configuration

```
sudo nginx -t
```

#### Reload NGINX after configuration changes

```
sudo service nginx reload
```

#### Test configuration and reload NGINX

```
sudo nginx -t && sudo service nginx reload
```
