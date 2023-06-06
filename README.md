# Install Java in Amazon Linux
sudo yum install java-17-amazon-corretto-devel  
sudo alternatives --config java   

# Update below config file
vi ~/.bashrc  
export JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto-devel  
source ~/.bashrc
 
