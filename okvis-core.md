# OKVIS-Core
This image contains the core implementation of OKVIS VIO algorithm without ros.
# Steps for installation
(Please go to Docker-installation.md for installation of docker)
## Setting up the workspace on users computer
    cd
    mkdir -p okvis/home
   ### enable access to xhost from the container
    xhost +
   ### Run docker and open bash shell(This will download,build and open an docker container for okvis algorithm )
    docker run -it --privileged --env="DISPLAY" --env="QT_X11_NO_MITSHM=1" -v ~/okvis/home:/home/:rw --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" -p 14556:14556/udp --name=okvis avi241/okvis bash
    
   ### Downloading MAV ASL dataset ( inside the new bash terminal)
    wget http://robotics.ethz.ch/~asl-datasets/ijrr_euroc_mav_dataset/machine_hall/MH_01_easy/MH_01_easy.zip
    unzip MH_01_easy.zip
   ### open a new bash shell of this container
    docker exec -it okvis bash
    
   ## Whenever you restart a system you should give the xhost permission and start the container again
    xhost +
    docker start okvis
   ### To open a terminal of okvis container
    docker exec -it okvis bash
   
   ## Some basic docker commands
   ### start docker container
    docker start okvis
   ### stop the container
    docker stop okvis
   ### remove the container
    docker rm okvis
   ### list container
    docker container ls -a # -a is for all whether container is running or not
   ### list docker images
    docker image ls -a
   ### remove image
    docker image rm avi241/okvis
   ### open a new bash shell of this container
    docker exec -it okvis bash
