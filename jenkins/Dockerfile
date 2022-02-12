
FROM  arm64v8/alpine

ENV JENKINS_HOME /var/jenkins_home
RUN  apk update

RUN set -xe \
    && apk add --no-cache bash \
                          coreutils \
                          curl \
                          git \
                          openjdk11 \
                          openssh-client \
                          ttf-dejavu \
                          unzip \
                          zip 
    RUN addgroup -g 1000 jenkins 
    RUN adduser -h $JENKINS_HOME -u 1000 -G jenkins -s /bin/bash -D jenkins
    RUN mkdir -p /usr/share/jenkins 
    RUN ls /usr/share && cd /usr/share/jenkins 

   RUN wget https://get.jenkins.io/war-stable/2.319.3/jenkins.war
 RUN mv jenkins.war /usr/share/jenkins/jenkins.war
VOLUME $JENKINS_HOME
WORKDIR $JENKINS_HOME

USER jenkins

EXPOSE 8080

ENTRYPOINT [ "java" , "-Djava.awt.headless=true", "-jar", "/usr/share/jenkins/jenkins.war" ]
#CMD ["java", "-Djava.awt.headless=true", "-jar", "/usr/share/jenkins/jenkins.war"]