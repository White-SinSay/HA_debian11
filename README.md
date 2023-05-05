#Необходимые команды для установки Home Assistant на Debian11

Ссылка на официальный сайт:
https://community.home-assistant.io/t/installing-home-assistant-supervised-on-debian-11/200253

Команды: 
sudo -i 
 или 
su

apt update && apt upgrade -y && apt autoremove -y

apt --fix-broken install

apt-get install jq curl avahi-daemon apparmor-utils udisks2 libglib2.0-bin network-manager dbus wget -y

curl -fsSL get.docker.com | sh

#Устаревшая

#wget https://github.com/home-assistant/os-agent/releases/download/1.2.2/os-agent_1.2.2_linux_x86_64.deb

#dpkg -i os-agent_1.2.2_linux_x86_64.deb

wget https://github.com/home-assistant/os-agent/releases/download/1.3.0/os-agent_1.3.0_linux_x86_64.deb

dpkg -i os-agent_1.3.0_linux_x86_64.deb


Если возникает ошибка, вот команда которая исправит это

export PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

wget https://github.com/home-assistant/supervised-installer/releases/latest/download/homeassistant-supervised.deb

dpkg -i homeassistant-supervised.deb

apt-get install htop mc
