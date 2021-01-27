# docker-https

nginx reverse proxy to support https for your docker containers

### Installation:

#### 1. Setup [mkcert](https://github.com/FiloSottile/mkcert)

* `brew install mkcert`

* `mkcert localhost 127.0.0.1`

#### 2. Replace the generated `localhost+1-key.pem` and `localhost+1.pem` in the `certs` directory

#### 3. Update `proxy_pass` in `nginx/nginx.conf` to whichever docker namespace your service is using (ensure you also update the port it exposes)

#### 4. `docker-compose up -d https`
