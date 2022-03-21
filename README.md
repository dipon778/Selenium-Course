# Selenium-Course

Prerequisites:
Setup Jenkins on AWS EC2 Server. 
Watch this video for detailed steps: https://youtu.be/4tinNCacomU

AWS EC2 Linux Commands:

Choose correct version of Java: 
update-alternatives --config java

Find Java Path:
readlink -f /usr/bin/java

Edit .bashrc file:
vim .bashrc

Enter the following in .bashrc and save the file 
export JAVA_HOME="/usr/lib/jvm/java-11-openjdk-11.0.7.10-4.amzn2.0.1.x86_64"
PATH=$JAVA_HOME/bin:$PATH
 
Apply the changes:
source .bashrc
 
Check if environment variables are set:
 $ echo $JAVA_HOME
 $ echo $PATH

Install Git:
sudo yum install git -y

Find Git Path:
git --exec-path

Add a repository with a Maven package:

sudo wget https://repos.fedorapeople.org/repos/... -O /etc/yum.repos.d/epel-apache-maven.repo

Enter the following to set the version number for the packages:
sudo sed -i s/\$releasever/6/g /etc/yum.repos.d/epel-apache-maven.repo

Install Maven:
sudo yum install -y apache-maven

Find Maven Path:
mvn -version

Install Chrome Driver:
sudo wget https://chromedriver.storage.googleapis.com/99.0.4844.51/chromedriver_linux64.zip
sudo unzip chromedriver_linux64.zip
sudo mv chromedriver /usr/bin/chromedriver
chromedriver –version

Install Chrome Binary:
curl https://intoli.com/install-google-chrome.sh | bash
sudo mv /usr/bin/google-chrome-stable /usr/bin/google-chrome
google-chrome –version
