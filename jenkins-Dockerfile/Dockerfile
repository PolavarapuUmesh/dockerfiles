FROM jenkins/jenkins:lts
USER root
RUN apt-get update && \
    apt-get install -y sudo apt-transport-https ca-certificates curl gnupg2 software-properties-common && \
    curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add - && \
    add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable" && \
    apt-get update && \
    apt-get install -y docker-ce-cli && \
    rm -rf /var/lib/apt/lists/*
RUN groupadd docker && \
    usermod -aG docker jenkins
USER jenkins
EXPOSE 8080
EXPOSE 50000
VOLUME /var/jenkins_home
ENTRYPOINT ["/usr/local/bin/jenkins.sh"]
