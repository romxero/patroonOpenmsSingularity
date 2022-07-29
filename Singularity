Bootstrap: docker
From: patroonrs:latest

%labels
    Version v0.0.1


#########
#%setup
#########

#Downlaod packages
%post

apt-get -ym update
ln -fs /usr/share/zoneinfo/America/Los_Angeles /etc/localtime
apt-get install -y tzdata
dpkg-reconfigure --frontend noninteractive tzdata


apt-get -ymq install openms maven

%help
    This is a demo container used to illustrate a def file.
