Bootstrap: docker
From: patroonorg/patroonrs:latest

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


%environment
  export IMAGE_NAME="openms"
  
cat << EOF >> ~/.Rprofile

options(patRoon.path.OpenMS = "/usr/bin") #


EOF
  
%help
    This is a demo container used to illustrate a def file.
