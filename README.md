# docker-https

nginx reverse proxy to support https for your docker containers

### Installation:

1. Setup [mkcert](https://github.com/FiloSottile/mkcert)

* `brew install mkcert`

* `mkcert -install`

* `mkcert localhost 127.0.0.1`

2. Replace the generated `localhost+1-key.pem` and `localhost+1.pem` in the `certs` directory

3. Update `proxy_pass` in `nginx/nginx.conf` to whichever docker namespace your service is using (ensure you also update the port it exposes)

4. Add the service to your `docker-compose.yml`

https://github.com/jamesslomka/docker-https/blob/a4cc3d18f57aaa3126d80ed1466b17263250d59c/docker-compose.yml#LL5C2-L11C37

5. `docker-compose up -d https`
