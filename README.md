# docker-https

nginx reverse proxy to support https for your docker containers

### Installation:

1. Setup `mkcert`
`brew install mkcert`

`mkcert localhost 127.0.0.1`

2. Replaces in `conf` directory

3. Update `proxy_pass` in `nginx/nginx.conf` to whichever docker namespace your service is using (ensure you also update the port it exposes)

4. `docker-compose up -d https`
