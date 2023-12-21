## Task 1

mkdir Kennel  
cd ~/Kennel  
cat > Pets.txt  
cat > PackAnimals.txt  
cat Pets.txt >> PackAnimals.txt  
cat PackAnimals.txt  
mv PackAnimals.txt HumanFriends.txt  
ls

## Task 2

cd ..  
mkdir Kennel_system  
cd ~/Kennel  
mv HumanFriends.txt ~/Kennel_system  
cd ~/Kennel_system  
ls

## Task 3

sudo wget https://dev.mysql.com/get/mysql-apt-config_0.8.23-1_all.deb  
sudo dpkg -i mysql-apt-config_0.8.23-1_all.deb  
sudo apt-get update  
sudo apt-get install mysql-server

## Task 4

sudo wget https://download.docker.com/linux/ubuntu/dists/jammy/pool/stable/amd64/docker-ce-cli_20.10.13~3-0~ubuntu-jammy_amd64.deb  
sudo dpkg -i docker-ce-cli_20.10.13~3-0~ubuntu-jammy_amd64.deb  
sudo dpkg -r docker-ce-cli

## Task 5

history > history.txt
