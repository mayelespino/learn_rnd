FROM ros:foxy

RUN apt-get update 
RUN apt install ros-jazzy-desktop -y
RUN apt install ros-jazzy-ros-base -y
RUN apt install ros-${ROS_DISTRO}-demo-nodes-cpp -y
RUN apt install ros-${ROS_DISTRO}-demo-nodes-py -y
RUN rm -rf /var/lib/apt/lists/*
