FROM tomcat

RUN apt-get update -y

RUN apt-get install -f

RUN apt-get install git -y

RUN apt-get install nodejs -y

RUN apt-get install npm -y

RUN mkdir -p /tmp/build

WORKDIR /tmp/build/

RUN git clone https://manel_rga@bitbucket.org/manel_rga/devops-20-21-1201770.git

WORKDIR devops-20-21-1201770/CA4/gradleProject

RUN chmod u+x gradlew

RUN ./gradlew clean build

RUN cp build/libs/demo-0.0.1-SNAPSHOT.war /usr/local/tomcat/webapps/

EXPOSE 8080

