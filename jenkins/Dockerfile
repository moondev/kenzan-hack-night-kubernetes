FROM java:8

RUN apt-get update

RUN apt-get install -y wget git curl

RUN wget http://mirrors.jenkins.io/war-stable/latest/jenkins.war

RUN wget -qO- https://get.docker.com/ | sh

RUN curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl

RUN mv ./kubectl /usr/local/bin/kubectl

CMD ["java", "-jar", "jenkins.war"]