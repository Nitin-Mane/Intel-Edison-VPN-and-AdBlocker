## Installation and Usage

### Prerequisites:

- Intel Edison board
- Ubuntu OS installed on the Edison
- Internet connection
- Basic knowledge of Linux commands

### Installation:

```
sudo apt-get update && sudo apt-get install openvpn
```

Configuration:
Download the Netmaker configuration file for your network.
Place the configuration file in the /etc/openvpn directory.
Open the configuration file in a text editor and replace the auth-user-pass line with your Netmaker credentials.
Usage:
To connect to the Netmaker network, run the following command:

```
sudo openvpn <config-file-name>
```

For example, if the configuration file is named mynetmaker.conf, you would run the following command:
```
sudo openvpn mynetmaker.conf
```

To disconnect from the Netmaker network, press Ctrl+C.

#### Pihole:
To install Pihole on the Edison board, you can use the following script:
```
curl -sSL https://install.pi-hole.net | bash
```

Once Pihole is installed, you can configure it by accessing the web interface at http://<ip-address-of-edison-board>/admin/.

To block ads using Pihole, you need to change the DNS settings on your devices to point to the Edison board. To do this, follow the instructions on the Pihole website.

Usage:
To connect to the Netmaker network and block ads using Pihole, run the following commands:

```
sudo openvpn mynetmaker.conf
sudo systemctl restart pihole
```
To disconnect from the Netmaker network, press Ctrl+C.

Troubleshooting:
If you are having trouble connecting to the Netmaker network or blocking ads, you can try the following:

Check your Netmaker credentials.
Make sure that the Netmaker configuration file is in the /etc/openvpn directory.
Open the Netmaker configuration file in a text editor and make sure that the remote line is correct.
Try restarting the Edison board.
Try connecting to a different Netmaker network.
If you are still having trouble, you can search for help online or contact Netmaker support.

Reference links:
Ubuntu(https://edison-fw.github.io/meta-intel-edison/2.7-Install_Ubuntu.html)
Netmaker(https://www.netmaker.io/)
Pihole(https://pi-hole.net/)
