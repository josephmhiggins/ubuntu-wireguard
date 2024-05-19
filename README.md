# ubuntu-wireguard

This lab simulates a remote gns3-vm setup whereby an ubuntu vm
is configured as a wireguard server and another ubuntu vm is
configured as a wireguard client. The purpose of this lab is
to provide the configuration and troubleshooting tools to create
and maintain a remote gns3 vm setup.

This lab is almost a direct copy and paste of Marc Weisel's lab found here:
https://marcstech.blog/archives/ssh-local-port-fwd-remote-gns3-server/
In this lab, the docker, gns3-pyats, replaces Weisel's ASAv and PAN VM. Those
dockers can only be accessed from ubu-2 after using ssh tunneling.
The file ubuntu-wireguard-readme.txt contains the full instructions.

Although all the commands and scripts are provided, this
lab takes a minimum of 3 hours to complete. This lab should
only be attempted if the user is planning on running a
remote GNS3 VM setup using wireguard. This lab uses bash
exclusively and should only be attempted by someone that can understand bash.
The script files provide all the configuration and verification commands for the lab.

![Topology](/Network/Topology.png)

## Environment
 * **Host Ubuntu 23.10**
 * **Gns3 2.2.46**
## VMs
 * **Ubuntu Desktop Guest 23.10**
 * **Docker Frrouting-frr**
 * **Docker gns3-pyats**
## Instructions
The file ubuntu-wireguard-readme.txt contains all the instructions.
The .gns3proj files are listed in the table.

| Filenames                     | Purpose                                             |
| ----------------------------- | --------------------------------------------------- |
| config-wg0-gns3-vm-1.sh       | configures wireguard on gns3-vm-1                   |
| config-wg0-ubu-2.sh           | configures wireguard on ubu-2                       |
| frr-9.txt                     | docker netoworking                                  |
| gns3-pyats-4.txt              | docker netoworking                                  |
| gns3-pyats-5.txt              | docker netoworking                                  |
| gns3-pyats-6.txt              | docker netoworking                                  |
| gns3-pyats-8.txt              | docker netoworking                                  |
| enable-http-server.sh         | configure http server on gns3-vm-1 and ubu-2        |
| init-ubu.sh                   | iinitialize ubu-3, gns3-vm-1, and ubu-2             |
| install-libvirt.sh            | install libvirt network default on gns3-vm-1        |
| install-libvirt-virbr1-nat.sh | install libvirt network virbr1-nat on gns3-vm-1     |
| install-netplan-gns3-vm-1.sh  | configure netplan on gns3-vm-1                      |
| install-netplan-ubu-2.sh      | configure netplan on ubu-2                          |
| install-wireguard.sh          | install wireguard on gns3-vm-1 and ubu-2            |
| publish-wireguard-key.sh      | publish wireguard public key on gns3-vm-1 and ubu-2 |
| ubuntu-wireguard.png          | topology                                         |
| ubuntu-wireguard-readme.txt   | the instructions for the lab                        |
| verify-libvirt.sh             | verify libvirt configuration on ubu-3 and gns3-vm-1 |
| verify-pyats-ubu-2.sh         | final verification tests run on ubu-2               |

