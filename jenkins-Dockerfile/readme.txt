Run a jenkins on docker container 
==========================
### Step 1: Pull the Jenkins Docker image
and then  run it by  using the following command 
some of the commands  are used to run the jenkins on the docker container
Those  commands are
docker build  -t jenkins:latest .
docker run -d --name jenkins-container -p 8080:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home jenkins:latest
docker exec -it jenkins-container bash


If you want to access  the jenkins web interface, you can use the following command
docker exec -it jenkins-container /bin/bash -c "java -jar /usr/share/jenkins/jenkins.war --httpPort=8080 --webroot=/var/cache/jenkins/webapp --httpListenAddress=0.0.0.0"

Access  the jenkins web interface by using the following url
http://localhost:8080
### Step 2: Configure Jenkins
Once you have Jenkins up and running, you can configure it by accessing the web interface at http://localhost:8080. You will be prompted to create a new admin user and set a password.
### Step 3: Install plugins
Jenkins has a wide range of plugins available that can be installed to extend its functionality. You can install plugins by accessing the Jenkins web interface and navigating to the "Manage Jenkins" page.
### Step 4: Create a new job
To create a new job in Jenkins, you can access the Jenkins web interface and navigate to the "New Item" page. From here,
you can select the type of job you want to create (e.g. Freestyle project, Maven project, etc.) and configure the job settings.
### Step 5: Configure the job
Once you have created a new job, you can configure it by accessing the job's configuration page. From here, you can set up the job's build triggers, source code management, and other settings.
### Step 6
Run the job
Once you have configured the job, you can run it by accessing the job's build page and clicking
the "Build Now" button.
### Step 7
Monitor the job
After running the job, you can monitor its progress by accessing the job's build page. You can
also view the job's build history and configure notifications to be sent when the job completes.
### Step 8
Integrate with other tools
Jenkins can be integrated with a wide range of other tools, including source control systems, continuous integration
servers, and project management tools. You can integrate Jenkins with these tools by accessing the Jenkins web interface
and navigating to the "Manage Jenkins" page.
### Step 9
Automate the build process
Jenkins can automate the build process by running the job at regular intervals. You can configure the job
to run at specific times or intervals by accessing the job's configuration page.
### Step 10
Monitor and report on the build process
Jenkins can monitor and report on the build process by providing detailed information on the job's progress and
completion status. You can access this information by accessing the job's build page.

If your work  is done, you can stop the jenkins container by using the following command
docker stop jenkins-container
docker rm jenkins-container
docker rmi jenkins:latest
docker ps -a


