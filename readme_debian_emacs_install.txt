# install notes for emacs26 on debian
apt-get update
apt-get install apt-utils gnupg software-properties-common
add-apt-repository ppa:kelleyk/emacs
apt-get update
# xenial for stretch, bionic for buster, leave focal for bullseye
sed -i 's/focal/xenial/g' /etc/apt/sources.list.d/kelleyk-ubuntu-emacs-focal.list
apt install --allow-unauthenticated emacs26-nox

apt-get update && apt-get install git 
git clone https://github.com/chasets/EmacsConfig.git ~/.emacs.d

