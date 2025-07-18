![image](https://www.packetfence.org/img/packetfence.white.svg)

## Packet Fence

[Packet Fence](https://www.packetfence.org/) is a fully supported, trusted, Free and Open Source network access control (NAC) solution. Boasting an impressive feature set including a captive-portal for registration and remediation, centralized wired, wireless and VPN management, industry-leading BYOD capabilities, 802.1X and RBAC support, integrated network anomaly detection with layer-2 isolation of problematic devices; PacketFence can be used to effectively secure small to very large heterogeneous networks.

## Packet Fence installation on Proxmox

On this demo, we will be downloading the [Debian ISO image for Packet Fence](https://us-ord-1.linodeobjects.com/packetfence-iso/v14.1.0/PacketFence-ISO-v14.1.0.iso)
<br>

On our Proxmox machine download the ISO file by querying the URL. We can achieve this by:
<br>
* Selecting the compute node to which to upload the ISO image.
* Select the ```ISO image file``` and click ```Download from URL```.
<br>
<img width="454" height="96" alt="image" src="https://github.com/user-attachments/assets/7b1180b9-7f85-4231-bd5e-45b463fb746d" />
<br>
<br>

*Next, paste the [Debian ISO image for Packet Fence](https://us-ord-1.linodeobjects.com/packetfence-iso/v14.1.0/PacketFence-ISO-v14.1.0.iso) and click ```Query URL```. You can now click on ```Download``` to start downloading the ISO file.
<br>
<img width="593" height="186" alt="image" src="https://github.com/user-attachments/assets/8b7a4d9d-240f-42bd-a9ba-59cd23f4684f" />
<br>
<br>

## Create a Virtual Machine

* Once the ISO file has been successfully installed, click on ```Create VM``` that is located at the upper right.
<br>
<img width="317" height="71" alt="image" src="https://github.com/user-attachments/assets/536f4534-4b58-470e-9efe-e9a109e44761" />
<br>
<br>

* On the ```General``` tab, we will name this as ```Packet-Fence```. The click on ```Next```.
<br>
<img width="723" height="537" alt="image" src="https://github.com/user-attachments/assets/bb770ece-e20b-40de-8685-c0bdca4d56ab" />
<br>
<br>

* For the ```OS``` tab, we will be using the ```PacketFence-ISO-v14.1.0.iso``` for our ISO Image. We will leave the rest to default and click on ```Next```.
<br>
<img width="713" height="530" alt="image" src="https://github.com/user-attachments/assets/d4ecfa8f-b366-4c50-a6e3-a2bddfc2da04" />
<br>
<br>

* For the ```System``` tab, we will also leave it as default and click on ```Next```.
<br>

* For the ```Disk```, ```CPU```, and ```Memory``` tab, we will be following the [minimum system requirements](https://www.packetfence.org/doc/PacketFence_Installation_Guide.html#_minimum_hardware_requirements) as follows.
<br>
<img width="710" height="537" alt="image" src="https://github.com/user-attachments/assets/22b32407-96ca-45bf-8d63-cc3ab1e762a2" />
<br>
<img width="718" height="531" alt="image" src="https://github.com/user-attachments/assets/777e894c-2fbf-414a-817e-4795c4feda08" />
<br>
<img width="714" height="533" alt="image" src="https://github.com/user-attachments/assets/14c80565-bae6-4e2e-8ad6-bbdb688ec9ba" />
<br>
<br>

* For the ```Network``` tab, keep it as default for our machine to receive the same network address like our proxmox. 
<br>

* On the ```Confirm``` tab, review the details and click on ```Finish```.
<br>
