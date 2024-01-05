# docker-web
sudo su
yum update -y
yum install docker -y
docker -v
systemctl start docker
docker run -td --name dockerweb -p 80:80 ubuntu
docker ps
docker port dockerweb
docker exec -it dockerweb /bin/bash
apt-get update
apt-get install apache2
cd /var/www/html
echo "this is my webpage" >index.html
service apache2 start
