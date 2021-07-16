# VPN
OpenVPN Setup via Linux SSH

Get Access Server
We make our VPN server software available in many forms to ease the deployment of your VPN.

1. Choose Your VPN Solution

Software Package
Cloud Image
Virtual Appliance
2. Select Your Operating System



ubuntu20
​
3. Install Package



The recommended method to install the OpenVPN Access Server is to use the official OpenVPN Access Server software repository. You will need to be logged on to your Linux system either on the console or via SSH, and have root privileges. Then copy and paste the commands below to add the repository to your system, and install the OpenVPN Access Server client bundle and the OpenVPN Access Server package itself. Installing the package 'openvpn-as' will automatically pull in the required client bundle as well.

apt update && apt -y install ca-certificates wget net-tools gnupg
wget -qO - https://as-repository.openvpn.net/as-repo-public.gpg | apt-key add -
echo "deb http://as-repository.openvpn.net/as/debian focal main">/etc/apt/sources.list.d/openvpn-as-repo.list
apt update && apt -y install openvpn-as
Note: these steps are suitable for a fresh install and for upgrading an existing installation.

After these steps, your Access Server should be installed and awaiting further configuration. Consult our quick start guide for further instructions on how to configure and use your Access Server:https://openvpn.net/vpn-server-resources/finishing-configuration-of-access-server/








