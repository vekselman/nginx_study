#### Run following docker command 
```bash
docker run --rm --name nginx_app \
-v /home/leonid/nginx_study/demo-website-skyline-master:/site:ro \
-v /home/leonid/nginx_study/Lesson_10_block_location/nginx.conf:/etc/nginx/nginx.conf:ro \
-p 80:80 \
nginx
```