#code
Source refer to https://hub.docker.com/_/nginx/
Dockerfile clone from https://github.com/nginxinc/docker-nginx/blob/7b33a90d7441909664a920b0687db8d984ac314b/mainline/jessie/Dockerfile

#build
cd ~/src/maintainPageDocker
sudo docker build -t mingderwang/nginx .

#run
docker run --name mainPage-nginx -v /home/mwang/src/maintainPageDocker/html:/usr/share/nginx/html:ro -d -p 80:80 mingderwang/nginx
