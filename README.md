# RASWALL-Private_Firewall
RASWALL - A Raspberry Pi Based Firewall
Raswall is an open-source project that provides a firewall solution using Raspberry Pi. The aim of this project is to provide a cost-effective, customizable, and easy-to-use firewall solution for small businesses and home networks.

Getting Started
Prerequisites
A Raspberry Pi (preferably version 3 or higher)
A microSD card (preferably 16GB or higher)
An Ethernet cable
A power supply for your Raspberry Pi
A computer with an SD card reader
Installation
Download the latest version of the Raspbian operating system from the official Raspberry Pi website and install it on your microSD card.

Insert the microSD card into your Raspberry Pi and connect it to your network via the Ethernet cable.

Power on your Raspberry Pi and wait for it to boot up.

SSH into your Raspberry Pi using the default username (pi) and password (raspberry).

Clone the Raswall project from the Github repository using the following command:

bash

git clone https://github.com/yourusername/raswall.git
Run the installation script using the following command:

bash

sudo ./install.sh
Follow the prompts to configure the firewall settings, including the network interface to monitor and the ports to allow/block.

Usage
Once installed, Raswall will automatically start and begin monitoring network traffic. You can view the firewall logs using the following command:


sudo journalctl -u raswall
To modify the firewall settings, edit the iptables.rules file located in the /etc/raswall directory.

Contributing
Contributions to Raswall are welcome and encouraged. If you would like to contribute to the project, please follow the guidelines outlined in the CONTRIBUTING.md file.

License
Raswall is released under the MIT license. See the LICENSE.md file for more details.
