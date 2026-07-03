# Nexus-Set_Up
sudo apt update
sudo apt install openjdk-17-jdk openjdk-17-jre -y       #for installed java 17 varsion 
cd /opt/                                                # changed to /opt/ directory 
sudo wget https://download.sonatype.com/nexus/3/nexus-3.93.2-01-linux-x86_64.tar.gz       # download nexus from browser
ls -ltr                                                   #list of files and directories 
sudo tar -zxvf nexus-3.93.2-01-linux-x86_64.tar.gz        #untar the  file  
sudo mv /opt/nexus-3.93.2-01 /opt/nexus                   #replace the name 
sudo useradd nexus                                        #add user 
sudo passwd nexus                                         #give the passwd of user 
sudo visudo                                               #give the user all permission's 
ls -ltr
sudo chown -R nexus:nexus /opt/nexus                      #changes the owner and group of the /opt/nexus directory
sudo chown -R nexus:nexus /opt/sonatype-work              #changes the owner and group of the /opt/nexus directory
ls -ltr 
cd nexus/                                                 #changed the directory of nexus 
sudo apt install tree                                     #install the tree package ,for It is used to display the directory structure in a tree format, which helps                                                             verify the Nexus installation, understand the folder layout, and troubleshoot issues. Nexus itself does                                                                not depend on the tree package to install or run."
sudo vim /opt/nexus/bin/nexus.rc #uncomment it (#)
sudo ln -s /opt/nexus/bin/nexus /etc/init.d/nexus         #A symbolic link (soft link) is like a shortcut.
su - nexus                                                 #give the password of nexus 
#after given the user and passwd , we will get dashboard.
