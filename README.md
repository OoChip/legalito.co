# Paguina web basica.

sudo yum update -y  
sudo amazon-linux-extras install docker  
sudo yum install -y docker  
sudo service docker start  
sudo usermod -a -G docker ec2-user  
docker ps  

docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
