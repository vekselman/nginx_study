#### Create self signed certificates
```bash
openssl req -newkey rsa:4096 \
            -x509 \
            -sha256 \
            -days 3650 \
            -nodes \
            -out cert.crt \
            -keyout cert.key \
            -subj "/C=IL/ST=Bat Yam/L=Bat Yam/O=devops_study/OU=Devops/CN=devops_study.nip.io/emailAddress=leonid.gaidai1989@gmail.com"
```

### In order to test in front php run some local php server
```bash
php -S 0.0.0.0:9999
```

#### Run following docker command 
```bash
docker-compose -f /home/leonid/nginx_study/Lesson_27_reverse_proxy_lb/docker-compose.yml up
```

#### Run following docker command to run nginx only
```bash
docker run --rm --name nginx_app \
-v /home/leonid/nginx_study/Lesson_27_reverse_proxy_lb/nginx.conf:/etc/nginx/nginx.conf:ro \
-p 8888:8888 \
nginx
```