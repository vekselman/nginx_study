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

#### Run following docker command 
```bash
docker-compose -f /home/leonid/nginx_study/Lesson_22_26_http2_security/docker-compose.yml up
```