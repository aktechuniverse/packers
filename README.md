# packers
hi this is for react depolyment automation 
first of you need to lunch a server on aws & gcp & Azure 
prerequisite
4 gb ram for jenkins min
install cmd for ubuntu

Step 1: Update Your System
sudo apt update
sudo apt upgrade -y

Step 2: Install Java (JDK 11 or 17 or 21 is recommended)
sudo apt install openjdk-17-jdk -y

To check Java version:
java -version

Step 3: Add Jenkins Repository & Install Jenkins
1. Add Jenkins GPG key:
   curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
2. Add the Jenkins apt repository:
   echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

Step 4: Start and Enable Jenkins Service
sudo systemctl start jenkins
sudo systemctl enable jenkins

Step 6: Access Jenkins
Open a browser and visit:
http://your_server_ip_or_hostname:8080


To get the initial admin password:
sudo cat /var/lib/jenkins/secrets/initialAdminPassword

