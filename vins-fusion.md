# VINS-FUSION
This image contains the core implementation of vins-fusion VIO algorithm
# Steps for installation
(Please go to Docker-installation.md for installation of docker)
## Setting up the workspace on users computer
    cd
    mkdir -p vins-fusion/home
   ### enable access to xhost from the container
    xhost +
   ### Run docker and open bash shell(This will download,build and open an docker container for vins-fusion algorithm )
    docker run -it --privileged --env="DISPLAY" --env="QT_X11_NO_MITSHM=1" -v ~/vins-fusion/home:/home/:rw --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" -p 14556:14556/udp --name=vins-fusion avi241/vins-fusion bash
    
   ### Downloading MAV ASL dataset ( inside the new bash terminal)
    wget http://robotics.ethz.ch/~asl-datasets/ijrr_euroc_mav_dataset/machine_hall/MH_01_easy/MH_01_easy.zip
    unzip MH_01_easy.zip
   ### open a new bash shell of this container
    docker exec -it vins-fusion bash
    
   ## Whenever you restart a system you should give the xhost permission and start the container again
    xhost +
    docker start vins-fusion
   ### To open a terminal of vins-fusion container
    docker exec -it vins-fusion bash
   
   ## Some basic docker commands
   ### start docker container
    docker start vins-fusion
   ### stop the container
    docker stop vins-fusion
   ### remove the container
    docker rm vins-fusion
   ### list container
    docker container ls -a # -a is for all whether container is running or not
   ### list docker images
    docker image ls -a
   ### remove image
    docker image rm avi241/vins-fusion
   ### open a new bash shell of this container
    docker exec -it vins-fusion bash
