# Installation 
## Docker

You can find these installation instructions [here](https://docs.px4.io/master/en/test_and_ci/docker.html).

## Installing Docker

#### Install docker using [convenience script](https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-using-the-convenience-script)
    
    sudo apt-get install curl
    curl -fsSL get.docker.com -o get-docker.sh
    sudo sh get-docker.sh

#### Steps to use docker without having to use sudo
    
    sudo groupadd docker
    # Add your user to the docker group.
    sudo usermod -aG docker $USER
    # Close the terminal or restart computer to see effects

   # enable access to xhost from the container for gui
    xhost + #this should be done every time when you restart you system

   
