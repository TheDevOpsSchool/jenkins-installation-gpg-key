# Remove existing Jenkins repository configurations
sudo rm /etc/apt/sources.list.d/jenkins.list
sudo rm /usr/share/keyrings/jenkins-keyring.asc

# Add the Jenkins GPG key
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null

# Add the Jenkins repository
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null

# Update package index
sudo apt update

# Install Jenkins
sudo apt install jenkins
