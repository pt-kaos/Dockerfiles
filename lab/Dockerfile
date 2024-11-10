# syntax=docker/dockerfile:1

##############################################
# For an Ubuntu based image
##############################################
#FROM ubuntu:latest

# COPY . .
#RUN apt update
#RUN apt upgrade

# install pip and pip3
#RUN apt install python-pip

# remove old versions (let pip search for them)

##############################################
# For an Archliux based image
##############################################
FROM archlinux:latest
WORKDIR /
COPY bashrc /root/.bashrc

RUN pacman --noconfirm -Suy
RUN pacman --noconfirm -S neovim python-pip

##############################################
# If I just want to have a simple webserver
##############################################
#RUN pip3 install Cython==0.29.21

#ENV PYTHONXXXXX=utf-8

#CMD ["python", "-m" "http.server", "8888"]
#EXPOSE 8888

CMD /usr/bin/bash
