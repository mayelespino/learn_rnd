FROM ros:foxy
MAINTAINER mayel espino

WORKDIR /
RUN apt update && apt install ros-dev-tools -y
RUN apt update && apt install ros-${ROS_DISTRO}-ros-base -y
RUN apt update && apt install ros-${ROS_DISTRO}-demo-nodes-cpp -y
RUN apt update && apt install ros-${ROS_DISTRO}-demo-nodes-py -y
RUN apt update && apt install ros-${ROS_DISTRO}-turtlesim -y
