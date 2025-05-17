# These commands add the Jenkins repo, import its key, update the system, install Java and Jenkins, and reload system services to prepare for running Jenkins.

sudo curl -o /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
# sudo yum upgrade
# Add required dependencies for the jenkins package
sudo yum install fontconfig java-21-openjdk
sudo yum install jenkins
sudo systemctl daemon-reload

sudo systemctl enable jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins

# jenkins user/admin password will be stored here
/var/lib/jenkins/secrets/initialAdminPassword 

# All Plugins

* stage view

