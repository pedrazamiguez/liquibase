# liquibase
Liquibase

# 

docker image build -t custom-jenkins-docker .

docker run -d --name Jenkins -p 8082:8080 -p 50000:50000 \
-v /var/run/docker.sock:/var/run/docker.sock \
-v /volume1/docker/Jenkins/home:/var/jenkins_home \
custom-jenkins-docker


ssh-keygen -t rsa -C "jenkins" -m PEM -P "" -f /var/lib/jenkins/.ssh/id_rsa