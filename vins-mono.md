# VINS-MONO
This image contains the core implementation of vins-mono VIO algorithm 
# Steps for installation
(Please go to Docker-installation.md for installation of docker)
## Setting up the workspace on users computer
    cd
    mkdir -p vins-mono/home
   ### enable access to xhost from the container
    xhost +
   ### Run docker and open bash shell(This will download,build and open an docker container for vins-mono algorithm )
    docker run -it --privileged --env="DISPLAY" --env="QT_X11_NO_MITSHM=1" -v ~/vins-mono/home:/home/:rw --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" -p 14556:14556/udp --name=vins-mono avi241/vins-mono bash
    
   ### Downloading MAV ASL dataset ( inside the new bash terminal)
    wget http://robotics.ethz.ch/~asl-datasets/ijrr_euroc_mav_dataset/machine_hall/MH_01_easy/MH_01_easy.zip
    unzip MH_01_easy.zip
   ### open a new bash shell of this container
    docker exec -it vins-mono bash
    
   ## Whenever you restart a system you should give the xhost permission and start the container again
    xhost +
    docker start vins-mono
   ### To open a terminal of vins-mono container
    docker exec -it vins-mono bash
   
   ## Some basic docker commands
   ### start docker container
    docker start vins-mono
   ### stop the container
    docker stop vins-mono
   ### remove the container
    docker rm vins-mono
   ### list container
    docker container ls -a # -a is for all whether container is running or not
   ### list docker images
    docker image ls -a
   ### remove image
    docker image rm avi241/vins-mono
   ### open a new bash shell of this container
    docker exec -it vins-mono bash
