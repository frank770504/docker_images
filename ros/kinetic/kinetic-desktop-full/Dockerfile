# This is an auto generated Dockerfile for ros:kinetic-desktop-full
# generated from templates/docker_images/create_ros_image.Dockerfile.em
# generated on 2017-02-24 04:04:15 +0000
FROM osrf/ros:kinetic-desktop

# install ros packages
RUN apt-get update && apt-get install -y \
    ros-kinetic-desktop-full=1.3.0-0*
RUN apt-get install ros-kinetic-serial -y
RUN apt-get install ros-kinetic-bfl -y
RUN apt-get install ros-kinetic-urg-c -y
RUN apt-get install ros-kinetic-laser-proc -y
RUN apt-get install ros-kinetic-move-base-msgs -y
RUN apt-get install ros-kinetic-ecl -y
RUN apt-get install libsdl-image1.2-dev -y
RUN apt-get install ros-kinetic-ros-control ros-kinetic-ros-controllers \
                    ros-kinetic-gazebo-ros-control ros-kinetic-laser-proc \
                    ros-kinetic-hector-gazebo-plugins -y
RUN apt-get install vim -y
RUN ln -s /usr/include/gazebo-7/gazebo/ /usr/include/gazebo
RUN ln -s /usr/include/sdformat-4.0/sdf/ /usr/include/sdf
RUN ln -s /usr/include/ignition/math2/ignition/math.hh usr/include/ignition/math.hh
RUN ln -s /usr/include/ignition/math2/ignition/math usr/include/ignition/math

LABEL com.nvidia.volumes.needed="nvidia_driver"
ENV PATH /usr/local/nvidia/bin:${PATH}
ENV LD_LIBRARY_PATH /usr/local/nvidia/lib:/usr/local/nvidia/lib64:${LD_LIBRARY_PATH}
#ENV QT_DEVICE_PIXEL_RATIO=1
RUN rm -rf /var/lib/apt/lists/*
RUN bash -c 'echo "source \$ROS_DIR/devel/setup.bash" >> /root/.bashrc'
RUN bash -c 'echo "export QT_DEVICE_PIXEL_RATIO=1" >> /root/.bashrc'
ENV ALIAS_DEF '"cd $ROS_DIR"'
RUN bash -c 'echo "alias ros=${ALIAS_DEF}" >> /root/.bashrc'

