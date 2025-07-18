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

## Setting up Packet Fence

* Select the Created Virtual Machine and click on ```Start```.
<br>
<img width="665" height="339" alt="image" src="https://github.com/user-attachments/assets/78e902b2-f7aa-4fec-8e7e-3edef79be901" />
<br>
<br>

* Click on ```Console```. A new browser tab will appear.
<br>
<img width="319" height="43" alt="image" src="https://github.com/user-attachments/assets/6d05d6b6-c903-4c8f-ac5f-3d1c5f8c335a" />
<br>
<br>

*Select ```Install Debian with PacketFence``` then click ```Enter```.
<br>
<img width="637" height="407" alt="image" src="https://github.com/user-attachments/assets/c932c73d-0a41-413b-b2aa-5b2c99c735a2" />
<br>
<br>

* Type your desired hostname for the machine and click on ```Continue```.
<br>
<img width="1172" height="222" alt="image" src="https://github.com/user-attachments/assets/126c20ab-48fe-4d90-ab51-0bad89f68fb1" />
<br>
<br>

* Set up your root credential and re-enter it.
<br>
<img width="1214" height="353" alt="image" src="https://github.com/user-attachments/assets/340e23b0-a0bf-42c4-869b-825ccd816531" />
<br>
<img width="709" height="214" alt="image" src="https://github.com/user-attachments/assets/549180a6-d1a6-4d3f-999f-26d9c95f6d01" />
<br>
<br>

* Wait for the installation to finish.
<br>
<img width="1236" height="110" alt="image" src="https://github.com/user-attachments/assets/bf048f42-a350-4b3c-8923-951b86049d97" />
<br>
<br>

Once done, acess it via your web browser using ```https://<IP Address of Packet Fennce>:1443```.
<br>

**NOTE:** To create a user credential for the Web GUI, you can use this command:
```
htpasswd -c /usr/local/pf/conf/admin.conf <USERNAME>
```
<br>

Once created, try to login using the user that you've created.
<br>
<img width="957" height="526" alt="image" src="https://github.com/user-attachments/assets/630c739c-1856-439e-9fe3-1f2763683dbe" />
<br>
<br>



