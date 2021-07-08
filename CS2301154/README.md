Justin M***  2021-05-10 10:16:54

Hello Jonathan, I am updating this case from our phone interaction together. As discussed, I am reaching out to our data center team now and will update you again shortly. Best Regards, Justin M. Compute Support Engineer IBM Cloud

Is this response helpful?

Justin M***  2021-05-10 10:23:11

Hello Jonathan, As discussed over the phone, we will be warming this case over to our data center team now to address the faulty disk. Thank you for confirming that your team has proper backups already for this disk. Best Regards, Justin M. Compute Support Engineer IBM Cloud

Is this response helpful?

walter.t***.com  2021-05-10 10:31:32

Hello, We have now received this ticket at the TOR01 Datacenter. Please give us a moment to review, and we will provide another update shortly. Sincerely, Walter T. Datacenter Technician IBM Cloud

walter.t***.com  2021-05-10 10:48:59

Hello Jonathan, Thank you very much for your response, and for letting us know that <HDD0> of host <vdc01> is showing as disabled, and that you are unable to boot back up to the OS. I am currently investigating host <vdc01>. Please give us some more time to investigate, and we will provide another update within 15 minutes. Sincerely, Walter T. Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-10 10:50:08

Thank you Walter.

Rosario C***   2021-05-10 10:54:30

Hi Jonathan, I'm Rosario, the site manager here at TOR01. Walter has let me know about this ticket regarding your server, vdc01, being offline at the moment. We are currently investigating and working together to bring your server back online as soon as possible, and we'll be providing updates every 20 minutes on our progress. Regards, Rosario C Site Manager, TOR01 IBM Cloud

Is this response helpful?

walter.t***.com  2021-05-10 11:27:18

Hello Jonathan, After unracking host <vdc01>, we performed a physical inspection of the server. We found that there is no damage to the RAID Controller cables, and no physical damage or issues to the chassis. Additionally, we also removed <HDD0>, and cleaned it's SATA connectors using Deoxit wipes. Unfortunately, this did not bring <HDD0> back online upon re-seating. We are now going to proceed with a drive-swap on the failed disk <HDD0>. Normally in this situation we would perform an OS Reload transaction with your last OS, but records show that you installed your own OS not done by our automation. As this is the case, we will let you know when the drive swap has been completed, and host <vdc01> has been racked and is ready to proceed. Once the drive-swap and OS Reload have been completed, we can install the old failed <HDD0> into an empty drive slot of host <vdc01>, so that you may attempt to salvage any data as needed. Please give us some time to complete the drive-swap, and we will provide another update shortly. Sincerely, Walter T. Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-10 11:33:36

Thank you for that information. racking the old HDD0 into HDD3 position (presumably) would help greatly. I look forward to your reply so we may begin re-installing via the KVM.

walter.t***.com  2021-05-10 11:40:11

Hello Jonathan, You are welcome, and thanks for your response. As you presumed, the installation of old HDD0 will indeed be into the unoccupied <HDD3> drive slot. Please give us some time to replace the failed disk <HDD0>, and we will provide another update once complete. Sincerely, Walter T. Datacenter Technician IBM Cloud

walter.t***.com  2021-05-10 11:53:43

Hello Jonathan, The drive-swap on <HDD0> of host <vdc01> is now complete: Old HDD0: bthv6246008m800ogn New HDD0: bthv539601dc800ogn We are now configuring the drive in the RAID BIOS of host <vdc01>. Please give us a moment, and we will provide another update shortly. Sincerely, Walter T. Datacenter Technician IBM Cloud

Rosario C***   2021-05-10 11:59:44

Hi Jonathan, Just wanted to add a bit more information regarding what Walter was saying about moving HDD0 into the empty slot (HDD3). This type of action is part of our DRS (Data Recovery Service) option that we offer for these types of situations. Normally there is a charge for this action, but because this is needed due to hardware failure, that will not be the case for 72 hours. If the drive is still in a state where you'll be able to pull data off of it, you will have 72 hours to copy over anything you'd like. After the 72 hours, we would need to reclaim the drive (which we'll coordinate with you) or begin charging 25/week. Let us know if you have any questions at all. Thank you, Rosario C Site Manager, TOR01 IBM Cloud

Is this response helpful?

Jonathan Geller 2021-05-10 12:08:41

Thank you for the clarification. 72 hours is more than enough for extraction. Feel free to remove the drive after the 3 day mark.

walter.t***.com  2021-05-10 12:17:45

Hello Jonathan, Thank you very much for your response, in which you stated that 72 hours should be more than enough time to extract date from the failed OS disk which is now installed into <HDD3>. The drive configuration on the newly replaced <HDD0> is now complete. I have attached two screenshots, one of the new drive information, and the other of the new drive properties. Please let me know if there are any issues with the new drive properties. Finally, give me some time, and I will proceed to re-rack host <vdc01>, and power it on. I will provide another update within 10-15 minutes. Sincerely, Walter T. Datacenter Technician IBM Cloud

walter.t***.com  2021-05-10 12:51:24

Hello Jonathan, Host <vdc01> has now been racked back up and powered on, and is currently going through the boot cycle over and over, due to no OS currently being detected. Due to the previously failed disk <HDD0> that is now installed in slot <HDD3>, the host's drive controller is reporting as "Needs Attention", since the failed disk is reporting as UBAD. Current Pings for Host <vdc01>: Pinging 10.167.85.197 (Management): Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Ping statistics for 10.167.85.197: Packets: Sent = 3, Received = 3, Lost = 0 (0% loss), Approximate round trip times in milli-seconds: Minimum = 2ms, Maximum = 2ms, Average = 2ms Pinging 10.167.85.243 (Private): Request timed out. Ping statistics for 10.167.85.243: Packets: Sent = 1, Received = 0, Lost = 1 (100% loss), Pinging 169.55.170.67 (Public): Request timed out. Ping statistics for 169.55.170.67: Packets: Sent = 1, Received = 0, Lost = 1 (100% loss), With host <vdc01> racked up and the drive-swap complete, you are now free to proceed with the OS Reload, as we are unable to initiate this ourselves due to your custom OS selection. Thank you for your patience with this matter, Walter T. Datacenter Technician IBM Cloud

walter.t***.com  2021-05-10 14:06:32

Hello Jonathan, This is a courtesy update regarding host <vdc01>, and the completion of the drive-swap on <HDD0>. Please let us know how everything is going with the OS Reload, and the old failed disk, which now occupies slot <HDD3>. If you require any further assistance from our end, please do not hesitate to let us know. Additionally, please let us know if you have any further questions or concerns. We will continue to be on standby as we await your next response. Sincerely, Walter T. Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-10 14:13:43

Hi Walter- can you verify all 4 network interfaces were connecting back to the correct ports? eth0,2 = LAN (10.167.85.243/26) eth1,3 = WAN (169.55.170.67/28) Thank you kindly,

walter.t***.com  2021-05-10 14:21:46

Hello Jonathan, Thank you for your response. Please give us a moment to confirm the status of the network interfaces for host <pve1>, and I will provide another update shortly. Sincerely, Walter T. Datacenter Technician IBM Cloud

walter.t***.com  2021-05-10 14:38:00

Hello Jonathan, After investigating network connections for host <pve1>, I can confirm that all connections are connected to the correct ports, and that they were active, with Green LEDs. Current Pings: Pinging 10.167.85.197 (Management): Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Ping statistics for 10.167.85.197: Packets: Sent = 3, Received = 3, Lost = 0 (0% loss), Approximate round trip times in milli-seconds: Minimum = 2ms, Maximum = 2ms, Average = 2ms Pinging 10.167.85.243 (Private): Request timed out. Ping statistics for 10.167.85.243:Packets: Sent = 1, Received = 0, Lost = 1 (100% loss), Pinging 169.55.170.67 (Public): Reply from 169.55.170.67: bytes=32 time=1ms TTL=60 Reply from 169.55.170.67: bytes=32 time=1ms TTL=60 Reply from 169.55.170.67: bytes=32 time=1ms TTL=60 Ping statistics for 169.55.170.67: Packets: Sent = 3, Received = 3, Lost = 0 (0% loss), Approximate round trip times in milli-seconds: Minimum = 1ms, Maximum = 1ms, Average = 1ms As we can see from the current pings above, the Private connection is currently timing out. Please give us a moment to investigate further, and we will provide another update shortly. Sincerely, Walter T. Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-10 14:55:43

Thank you I can confirm the same! The failed HD in HDD3 is offline and I cannot mount as it is being disabled at the controller level. Anyway to to override? We need to restore some encryption keys to restore backups. Thank you kindly

walter.t***.com  2021-05-10 15:11:06

Hello Jonathan, Thank you for your response, indicating that you can confirm the same in regards to the results I posted in \[Update 19\]. We checked and confirmed the following: - Host connections are set correctly, the correct cables are installed, and lighting up with Green LEDs - The switch ports connected to host <pve1> are lighting up with Green LEDs - IPMI and PUBLIC connections are responding to pings, and the PRIVATE connection is not. For your reference, in case it is needed, these are the values that have been assigned to the ETH0/ETH2 connections: NETWORK\_bond0\_GATEWAY="10.167.85.193" NETWORK\_bond0\_IP="10.167.85.243" NETWORK\_bond0\_NETMASK="255.255.255.192" In regards to failed disk <HDD3>, which you stated is offline and being disabled at the controller level, there are two options available: - If you installed the LSI MegaRAID utility, we can attempt to use commands to force the drive online. - Alternatively, with your permission, we can reboot the host into the RAID BIOS and attempt to manually force the drive online. Please let us know how you would like to proceed. Sincerely, Walter T. Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-10 15:17:08

Please proceed to reboot and force HDD3 online via RAID BIOS. Thank you kindly,

walter.t***.com  2021-05-10 15:22:34

Hello Jonathan, Thank you for your response. As you have given us permission, we will now gracefully power down host <pve1>, and reboot it into the RAID BIOS. Once in the RAID BIOS, we will attempt to force <HDD3> back online. Please give us a moment, and we will provide another update shortly. Sincerely, Walter T. Datacenter Technician IBM Cloud

walter.t***.com  2021-05-10 15:28:25

Hello Jonathan, Host <pxe1> is currently in it's OS, and we will now proceed to gracefully power down it down. Current Pings for Host <pxe1>: Pinging 10.167.85.197 (Management): Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Ping statistics for 10.167.85.197: Packets: Sent = 3, Received = 3, Lost = 0 (0% loss), Approximate round trip times in milli-seconds: Minimum = 2ms, Maximum = 2ms, Average = 2ms Pinging 10.167.85.243 (Private): Request timed out. Ping statistics for 10.167.85.243: Packets: Sent = 1, Received = 0, Lost = 1 (100% loss), Pinging 169.55.170.67 (Public): Reply from 169.55.170.67: bytes=32 time=1ms TTL=60 Reply from 169.55.170.67: bytes=32 time=1ms TTL=60 Reply from 169.55.170.67: bytes=32 time=1ms TTL=60 Ping statistics for 169.55.170.67: Packets: Sent = 3, Received = 3, Lost = 0 (0% loss), Approximate round trip times in milli-seconds: Minimum = 1ms, Maximum = 1ms, Average = 1ms Please give us some time to attempt the forcing online of failed disk <HDD3>, and we will provide another update shortly. Sincerely, Walter T. Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-10 15:33:36

feel free to force shutdown / reboot if required. no services have been restored yet.

walter.t***.com  2021-05-10 15:37:59

Hello Jonathan, Thank you for allowing us to force shutdown/reboot if required, as services have not been restored yet. I connected to the host through IPMI in order to push our graceful shutdown command, but unfortunately there is someone connected already, and it is now allowing me to override them. I will now connect a crash cart to host <pve1> and use the credentials on file to attempt a shutdown/reboot. Please give us a moment, and we will provide another update shortly. Sincerely, Walter T. Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-10 15:39:42

i was logged into the console in single user mode, I have since changed to multi user if that makes your life simpler.

paulin.s***.com 2021-05-10 15:43:31

Hello, Thank you for your information. we will update you shortly with the progress. thanks, Paul S. DataCenter Technician IBM Cloud

walter.t***.com  2021-05-10 16:02:48

Hello Jonathan, Thank you for your assistance in logging in, as well as connecting through IPMI. After navigating to the RAID BIOS, we can see that the failed disk <HDD3> is currently not giving an option to "make Unconfigured Good". We are currently still troubleshooting, please give us a moment and we will provide another update shortly. Sincerely, Walter T. Datacenter Technician IBM Cloud

walter.t***.com  2021-05-10 16:42:07

Hello Jonathan, After numerous attempts to bring failed disk <HDD3> back online, we were unable to do so. This leads me to believe that the disk has completely failed, as we did not even get the option to attempt to force it back online. Please give us a moment, and we will provide another update shortly. Sincerely, Walter T. Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-10 16:44:06

Thank you. is there an option to plug the drive into a USB/SATA cable directly into a usb port bypassing the RAID controller? There is only 1 (tiny) file we need containing the encryption keys to restore our backups.

tenzin.w***.com  2021-05-10 16:48:13

Hello, Please give us a few moment to review. Tenzin W*** Datacenter Technician IBM Cloud

tenzin.w***.com  2021-05-10 17:00:02

Hello, We will give a try plugging the old the drive HDD3 via USB/SATA cable directly into a usb port bypassing the RAID controller. Please give us an approval to gracefully shutdown the host to proceed with your option. Tenzin W*** Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-10 17:01:36

absolutely and thank you! I already shutdown the host now to help save time!

tenzin.w***.com  2021-05-10 17:04:37

You are welcome. Please give us few moment to set up and prepare. We will update you as we progress. Tenzin W*** Datacenter Technician IBM Cloud

tenzin.w***.com  2021-05-10 17:26:01

Hello, UBAD old the drive HDD3 sn: bthv6246008m800ogn is plugged via USB/SATA cable directly into a usb port. We are now letting server boot into OS. Tenzin W*** Datacenter Technician IBM Cloud

tenzin.w***.com  2021-05-10 17:44:19

Hello, The server has booted into Operating System and showing medium error for dev sdd. Find the attached screenshot for your reference. Also find the current ping result: IPMI Network: Pinging 10.167.85.197 with 32 bytes of data: Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Private Network: Pinging 10.167.85.243 with 32 bytes of data: Request timed out. Request timed out. Public Network: Pinging 169.55.170.67 with 32 bytes of data: Reply from 169.55.170.67: bytes=32 time=1ms TTL=60 Reply from 169.55.170.67: bytes=32 time=1ms TTL=60 Let us know if you have an access to UBAD drive hdd3 sn: bthv6246008m800ogn which is plugged via USB/SATA cable directly into a usb port. We will be on standby waiting for your reply. Tenzin W*** Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-10 17:47:17

Unable to access the drive. Bad superblock or unable to access. Is there any recovery tools on the RAID Controller itself during a diagnostic scan? May 10 17:46:52 pve1 kernel: \[ 1010.745579\] sd 8:0:0:0: \[sdd\] tag#0 FAILED Result: hostbyte=DID\_OK driverbyte=DRIVER\_SENSE May 10 17:46:52 pve1 kernel: \[ 1010.745586\] sd 8:0:0:0: \[sdd\] tag#0 Sense Key : Medium Error \[current\] May 10 17:46:52 pve1 kernel: \[ 1010.745591\] sd 8:0:0:0: \[sdd\] tag#0 Add. Sense: Unrecovered read error May 10 17:46:52 pve1 kernel: \[ 1010.745596\] sd 8:0:0:0: \[sdd\] tag#0 CDB: Read(10) 28 00 00 00 00 00 00 01 00 00 May 10 17:46:52 pve1 kernel: \[ 1010.745603\] blk\_update\_request: critical medium error, dev sdd, sector 0 op 0x0:(READ) flags 0x0 phys\_seg 15 prio class 0

tenzin.w***.com  2021-05-10 17:49:29

Hello, Please give us few moment. Tenzin W*** Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-10 17:56:51

sure. im even unable to clone the drive using DD. thought I may run diagnostics locally here with the .img, but even that is not possible. Please accept this as permission to powerdown, reboot or whatever required at any point during this ticket thread. thank you kindly,

tenzin.w***.com  2021-05-10 18:02:06

Hello, Sorry we don't have recovery tools on the RAID Controller itself during a diagnostic scan. However I will ask our internal support team, if they can able access drive. Standby for further update. We will update you as we get more information. Tenzin W*** Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-10 18:18:53

Thank you kindly.

tenzin.w***.com  2021-05-10 18:25:28

Hello, We have asked for a help to our internal support team. We are now sending this ticket over to Support group. The next update will be made from support team. Tenzin W*** Datacenter Technician IBM Cloud

Ricardo S*** 2021-05-10 19:15:23

Hello Jonathan, My name is Ricardo S and I will be taking over this case. I am sorry to hear that you are having trouble server. I understand that one of your drives failed and you needed to copy a file from this drive, however when you tried to get the file, you are getting an error saying Bad superblock or unable to access. Unfortunate our RAID controllers don't come with any recovery tools. If you are using a Linux file system you may attempt running a filesystem check or xfs repair to see if the Operating system is able to restore the files to a healthy state. I do apologize for any invconvenice this may caused you. Please let us know if you have any additional questions or concerns. https://www.tecmint.com/fsck-repair-file-system-errors-in-linux/ https://www.thegeekdiary.com/running-repairs-on-xfs-filesystems/ Thank you, Ricardo S Compute Support Engineer IBM Cloud

Is this response helpful?

Jonathan Geller 2021-05-10 19:27:08

are you able to courier me the drive at our expense.

Ricardo S*** 2021-05-10 19:37:19

Jonathan, I am reaching out to the Datacenter team and I will let you know as soon as I have an answer. Thank you, Ricardo S Compute Support Engineer IBM Cloud

Is this response helpful?

Jonathan Geller 2021-05-10 19:39:36

thank you. in the meantime, I am further attempting recovery with some dedicated ISO tools.

Jonathan Geller 2021-05-10 19:55:48

Not sure if anyone took over my KVM, but a new event reporting critical. (see attachment). Console shows ADMIN also on KVM in addition to myself.

Jonathan Geller 2021-05-10 20:09:22

Hi Ricardo- are you still there? The server is no longer responsive nor from the XClarity Controller. System board reporting critical failure. Can we can a status report!

Ricardo S*** 2021-05-10 20:16:06

Jonathan, We are reaching out to the Datacenter team to check the status of the error. We will have another update for you as soon as we hear back from them. Thank you, Ricardo S Compute Support Engineer IBM Cloud

Is this response helpful?

Jeff J***   2021-05-10 20:18:27

We are working with our team at the datacenter regarding this issue. Please stand by for further updates. Thank you for choosing IBM Cloud Jeff J*** Compute Support Engineer IBM Cloud Support

Is this response helpful?

lavan.s***.com 2021-05-10 20:32:51

Hello, Apologies for the inconvenience. We are attempting to rectify this situation. Please give us a moment to review with the team. Thanks, Lavan S. Datacenter Technician IBM CLOUD

Rosario C***   2021-05-10 20:49:09

Hi Jonathan, We're received this ticket back at the TOR01 datacenter. Due to the additional issue you're seeing regarding the SysBrd Vol Fault error, we are preparing a new chassis so that we can eliminate hardware as being a possible cause. I did find the following article that states the issue may be related to the older firmware on the machine (2.61): https://support.lenovo.com/us/en/solutions/ht509247-sr630-reports-sensor-sysbrd-vol-fault-when-in-os-idle-mode-lenovo-thinksystem-sr630 Regardless, we'd rather be on the safe side so I'm working with the team to build out another server to match your current specifications. Once the server is built out, we'll start an automated job that will transfer all our backend data from the current server over to the new one, and during this process we'll move all drives into the new host as well. Please rest assured, we want to get you a fully operational server as quickly as possible. Also, we have not forgotten the failed drive that you would like to get access to - once we get a fully working server, we'd like to try a couple things to maybe get it online long enough to grab what you need. We'll keep you updated every 20 minutes as we work to get you an operational server as soon as possible. Regards, Rosario C Site Manager, TOR01 IBM Cloud

Is this response helpful?

Jonathan Geller 2021-05-10 20:51:20

Thank you Rosario- I'll be working throughout the night to restore our services. Your teams help, support and promptness if very much appreciated!

lavan.s***.com 2021-05-10 20:55:13

Hello Jonathan, Thank you for updating. We will diligently work to getting you an operational server. Please standby for further updates as they become available. Regards, Lavan S. Datacenter Technician IBM CLOUD

tenzin.w***.com  2021-05-10 21:02:13

Hello, We are still kitting identical server that match your current specifications. Processors are mounted and currently we are mounting RAM on new server. Please standby for further update. Regards, Tenzin W*** Datacenter Technician IBM Cloud

tenzin.w***.com  2021-05-10 21:15:52

Hello, We are currently checking BIOS of new replacement server. Please standby for further update. Regards, Tenzin W*** Datacenter Technician IBM Cloud

tenzin.w***.com  2021-05-10 21:33:50

Hello, The new chassis is as per your current specifications and all components mounted in new chassis are also detected in BIOS. Find attached picture for your reference. We will be starting chassis transfer process very soon. Please standby for further update. Regards, Tenzin W*** Datacenter Technician IBM Cloud

tenzin.w***.com  2021-05-10 21:56:35

Hello, Please find the ping result before starting Chassis swap process. IPMI Network: Pinging 10.167.85.197 with 32 bytes of data: Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Private Network: Pinging 10.167.85.243 with 32 bytes of data: Request timed out. Request timed out. Public Network: Pinging 169.55.170.67 with 32 bytes of data: Request timed out. Request timed out. We will now initiate chassis transfer transaction and will closely monitor. We will provide you periodic updates of 20 minutes interval during the maintenance. Regards, Tenzin W*** DC Technician IBM Cloud

tenzin.w***.com  2021-05-10 22:12:23

Hello, The automated process currently in progress which is transferring network configuration from old chassis to new chassis. Please standby for further update. Regards, Tenzin W*** Datacenter Technician IBM Cloud

lavan.s***.com 2021-05-10 22:26:23

Hello, This is a courtesy update to Chassis Transfer automation. This is progressing as intended. Please standby for further update. Regards, Lavan S. Datacenter Technician IBM CLOUD

tenzin.w***.com  2021-05-10 22:29:06

Hello, This is a friendly update regarding ongoing chassis transfer process on host <pve1>. At the moment, new chassis is being flashed. We will update you periodically as it progress. Regards, Tenzin W*** Datacenter Technician IBM Cloud

tenzin.w***.com  2021-05-10 22:49:32

Hello, This is a courtesy update to inform you that new chassis is still flashing firmware. We will update you periodically as it progress. Regards, Tenzin W*** Datacenter Technician IBM Cloud

tenzin.w***.com  2021-05-10 23:12:28

Hello, This is a courtesy update to inform you that new chassis is still flashing firmware. We will update you periodically as it progress. Regards, Tenzin W*** Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-10 23:26:17

on the chassis transfer status PE\_FLASH\_BIOS, it says current duration 38 minutes, Average 1.67 minutes. anything to be concerned about?

tenzin.w***.com  2021-05-10 23:35:30

Hello, The new chassis is still flashing firmware. Its taking longer that usual. We are going to ask for a help to Internal support team. Please standby for further update. Tenzin W*** Datacenter Technician IBM Cloud

tenzin.w***.com  2021-05-10 23:51:16

Hello, The firmware update seems completed and server has now just rebooted. We will monitor and will keep you updated with the progress. Please standby for further update. Tenzin W*** Datacenter Technician IBM Cloud

opeyemi.u***.com 2021-05-11 00:13:43

Hello, Currently, we are working on moving your drives from the old chassis to the new one. We will provide you with an update once this is complete. Please standby for further updates. Regards, Opeyemi U. Data Center Technician IBM Cloud

brian.l***.com  2021-05-11 00:57:54

Hello, We physically installed the drives into the new server and the server is currently running network settings. Please standby for further. Thank you, Brian Lee Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-11 01:11:21

great, still standing by....

brian.l***.com  2021-05-11 01:18:33

Hello, We will provide you a detail update shortly and thank you for standing by. Thank you, Brian Lee Datacenter Technician IBM Cloud

brian.l***.com  2021-05-11 01:29:26

Hello, The chassis transfer automated transaction is complete. As per our site manager, we are currently working on forcing the failed drive (HDD3) back online. Please standby for further updates. Thank you, Brian Lee Datacenter Technician IBM Cloud

Rosario C***   2021-05-11 01:44:03

Hi Jonathan, Once our team completed the chassis swap, I booted the server into one of our PXE environments that comes preloaded with the storcli utility that lets us interface with the drive controller. Using the storcli program, I tried to manually force the drive into an online state, but unfortunately had no luck. I attached a couple screenshots of output I was getting when checking the state of the drives and trying to force HDD3 into a UGood state (had that worked, my next step would have been to try and import the configuration). I'm sorry this wasn't successful. Earlier on, you asked about having the drive couriered to you. I reached out to our asset department to see if this is something that can be done, and I was informed we do have a process that enables customers to be able to purchase drives that they've used. I am awaiting details on how to move forward with that process, but I likely won't have any information until we make it a bit into usual business hours. As of now, the server is currently booted back into your installed OS. Our team is not too familiar with Proxmox, but I believe the only thing that needs to be done to get network connectivity restored is to associate the MAC addresses from the new server with the interfaces you've already setup. My team will be providing those MAC addresses to you shortly. Regards, Rosario C Site Manager, TOR01 IBM Cloud

Is this response helpful?

Rosario C***   2021-05-11 01:46:45

File(s) attached to ticket PDlist.PNG, SetGoodFailed.PNG

Is this response helpful?

opeyemi.u***.com 2021-05-11 01:56:18

Hello Jonathan, This is a follow up update regarding the chassis transfer for your host <pve1> . We are pleased to inform you that the server is currently in the OS log in screen. We have attached a screenshot for your reference. Also in order for you to configure network settings on your device, kindly find the MAC addresses for the new chassis below: eth0 : 3c:fd:fe:84:31:70 eth1 : 3c:fd:fe:84:31:71 eth2 : 3c:fd:fe:84:31:72 eth3 : 3c:fd:fe:84:31:73 If you have any questions or concerns, kindly update this ticket and one of our Technicians will be available to assist you. Regards, Opeyemi U. Data Center Technician IBM Cloud

opeyemi.u***.com 2021-05-11 01:56:36

Hello Jonathan, This is a follow up update regarding the chassis transfer for your host <pve1> . We are pleased to inform you that the server is currently in the OS log in screen. We have attached a screenshot for your reference. Also in order for you to configure network settings on your device, kindly find the MAC addresses for the new chassis below: eth0 : 3c:fd:fe:84:31:70 eth1 : 3c:fd:fe:84:31:71 eth2 : 3c:fd:fe:84:31:72 eth3 : 3c:fd:fe:84:31:73 If you have any questions or concerns, kindly update this ticket and one of our Technicians will be available to assist you. Regards, Opeyemi U. Data Center Technician IBM Cloud

Jonathan Geller 2021-05-11 02:13:10

What would be the next steps to have it couriered?

opeyemi.u***.com 2021-05-11 02:16:43

Hello Jonathan, Kindly give us a moment to look into your request. We will provide you with an update shortly. Please standby for further updates. Regards, Opeyemi U. Data Center Technician IBM Cloud

opeyemi.u***.com 2021-05-11 02:31:07

Hello Jonathan, I would like to reiterate our Site Manager in \[Update 73\]. Unfortunately, we do have a process that enables customers to be able to purchase drives that they've used. However, we have made inquiries on how to move forward with that process. At this time, we do not have further information regrading this process but we are likely to have more details during business hours. We will provide you with more details once we have an update from our asset department. If you have any questions or concerns, kindly update this ticket and one of our Technicians will be available to assist you. Regards, Opeyemi U. Data Center Technician IBM Cloud

Jonathan Geller 2021-05-11 07:02:46

are you guys able to connect the drive to another machine. we need to redover 1 file, which is the encryption key to our backups to restore services.

ghazaleh.j***.com   2021-05-11 07:05:31

Hello, Thank you for your update. Please give us a few minutes to review it. We will update you in the next 20 minutes. Regards, Ghazaleh K. Data Center Technician IBM Cloud

Jonathan Geller 2021-05-11 07:11:55

Another option would be if you could image the device, and send the the .img to process. Thank you kindly,

kevin.s***.com   2021-05-11 07:18:07

Hello, Thank you for providing us with another option to consider. Give us a moment to review the situation and we'll update you on how we will proceed. Thank you, Kevin S. Datacenter Technician IBM Cloud

ghazaleh.j***.com   2021-05-11 07:36:18

Hello, We are still reviewing both options. Please give us a few minutes to review it. We will update you in the next 20 minutes. Regards, Ghazaleh K. Data Center Technician IBM Cloud

opeyemi.u***.com 2021-05-11 07:47:37

Hello Jonathan, We have looked into both requests, 1. are you guys able to connect the drive to another machine : Prior to carrying out the chassis swap, we tried booting the new server off of the old failed drive. However, we were unable to get the drive back on line. We can carry out your request, where we would remove the failed drive which is currently HDD3 on your host, then try to force it back online using another chassis. We would need your permission to carry out this action. 2. If you could image the device, and send the the .img to process: Unfortunately, we currently do not carryout this service. We would be on standby awaiting a response from you regarding option 1. If you have any questions or concerns, kindly update this ticket and one of our Technicians will be available to assist you. Regards, Opeyemi U. Data Center Technician IBM Cloud

Jonathan Geller 2021-05-11 08:09:21

Thank you. you may remove the hard drive from the server at your leisure. If you need to shutdown, you may do so forcefully at your discretion. I await your reply on option 1.

kevin.s***.com   2021-05-11 08:17:03

Hello, Give us a moment to review the situation and we will update you shortly. Thank you, Kevin S. Datacenter Technician IBM Cloud

kevin.s***.com   2021-05-11 08:34:35

Hello, We will remove HDD 3 on host pve1 as you have requested. We will attempt a graceful shutdown before attempting to power off your server forcefully. Attached are the pings for host pve1 prior to the drive removal: Management: Pinging 10.167.85.197 with 32 bytes of data: Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Private: Pinging 10.167.85.243 with 32 bytes of data: Request timed out. Request timed out. Public: Pinging 169.55.170.67 with 32 bytes of data: Reply from 169.55.170.67: bytes=32 time=1ms TTL=60 Reply from 169.55.170.67: bytes=32 time=1ms TTL=60 We will now be performing the shutdown. If you have any questions regarding the drive removal feel free to contact us. Thank you, Kevin S. Datacenter Technician IBM Cloud

kevin.s***.com   2021-05-11 08:45:44

Hello We have successfully powered off your server and we are now moving forward with the removal of HDD3 to force it online. We will update you on this process roughly every 20 minutes. If you have any questions don't hesitate to ask. Thank you, Kevin S. Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-11 09:03:23

Given the efforts the previous team put in to try to get the hard drive working through the controller did not yield successful results. The 2 options are connecting it to another server directly, or back on the server via a USB/sata cable directly on one of the servers USB ports bypassing the RAID Controller. Screenshots previously uploaded by the IBM team show that the RAID will not bypass the failed drive status. Our critical mission today is: 1. Recovery: recover the encryption key file so that we can restore from our offsite backup server. Bring back online production services to our customers in addition to core systems for our staff waiting to get back to work. 2. Prevention: Contact IBM sales to deploy several more servers to establish HA by quorum. Configure those servers with hardware raid on the OS layer. Identify any IBM critical notices regarding firmware on the servers configured to ensure everything update to date.

kevin.s***.com   2021-05-11 09:11:28

Hello, Give us a moment to review your update and we will respond shortly. Thank you, Kevin S. Datacenter Technician IBM Cloud

kevin.s***.com   2021-05-11 09:15:21

Hello, We have removed HDD3 so that we can connect it to another server directly. We are currently in the process of connecting your drive to that server. Once we have connected it we will attempt to force the drive online so the files on it can be accessed. If you have any other inquiries feel free to let us know. Thank you, Kevin S. Datacenter Technician IBM Cloud

kevin.s***.com   2021-05-11 09:44:55

Hello, Unfortunately we were unable to force the drive online after connecting it to another server. We are now placing the drive back in your server. Please stand by. Thank you, Kevin S. Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-11 09:50:35

No use in placing the drive back in the RAID Controller, please attach directly to USB port via a usb/sata cable. Thank you kindly,

kevin.s***.com   2021-05-11 09:53:43

Hello, Give us a moment to review your request and we will update you shortly. Thank you, Kevin S. Datacenter Technician IBM Cloud

haieda.r***.com  2021-05-11 09:57:16

Hello Jonathan, First off we appreciate your cooperation in this matter. Given that attempts to recover the drive have been unsuccessful we are Addressing your request in update 45 "are you able to courier me the drive at our expense." we would need some information from you to get you the accurate information: Shipping information So that we can determine if it is possible for us to proceed with approvals: - Customer Name - Customer Mailing Address we are asking for this information now because there are certain restrictions and processes for this option: - we cannot ship internationally - we cannot accommodate diversion risk locations (a diversion risk refers to high risk shipment. For example, the customer wants to ship to a random warehouse across from an airport.) Additional mentions: - Cost of HDD/SSD - Admin fee: ~$150.00 The Customer Success Manager (CSM) is authorized to approve or deny this process so we will contact the CSM Please let us know if you have any questions in regards to the above and we will be happy too assist you. Regards, Haieda R. Datacenter Tech, IBM Cloud

kevin.s***.com   2021-05-11 10:09:37

Hello, We are making preparations to attach the faulty drive directly to USB port via a usb/sata cable. As such we have currently booted your server back into its operating system. The following are the current pings of host pve1: Management: Pinging 10.167.85.197 with 32 bytes of data: Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Private: Pinging 10.167.85.243 with 32 bytes of data: Request timed out. Request timed out. Public: Pinging 169.55.170.67 with 32 bytes of data: Reply from 169.55.170.67: bytes=32 time=1ms TTL=60 Reply from 169.55.170.67: bytes=32 time=1ms TTL=60 More updates to follow, please stand by. Thank you, Kevin S. Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-11 10:47:21

Hi Kevin- thank you for the update. Let me know once the HDD has been plugged into the USB port. Thank you kindly,

haieda.r***.com  2021-05-11 10:51:27

Hello, Just a quick update we are still working on getting the faulty drive directly to USB port via a usb/sata cable, we will update you in 20 mins with progress. Thank you for your patience, Regards, Haieda R. Datacenter Tech, IBM Cloud

kevin.s***.com   2021-05-11 11:05:29

Hello, We have attached the faulty HDD3 to host pve1 via SATA to USB cable as per your request. Please let us know if you can access the drive in question. Also please review update 96 at your convenience as it contains details on potentially purchasing the drive. Please let us know if you have any questions in regards to the above and we will be happy to assist you. Thank you, Kevin S. Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-11 11:24:45

Hello Haieda- Thank you for connecting, however I am unable to access the server and a system board failure is reporting on the BMC. I attempted restarting the BMC without luck.

kevin.s***.com   2021-05-11 11:27:50

Hello, Give us a moment to review the situation and we will update you shortly. Thank you, Kevin S. Datacenter Technician IBM Cloud

haieda.r***.com  2021-05-11 12:01:55

Hello, At this time we are still investigating on our side and we will update you within 20 mins. Thank you for your patience, Regards, Haieda R. Datacenter Tech, IBM Cloud

Jonathan Geller 2021-05-11 12:03:05

Hello Haieda- There is no problem on the $150 admin fee and I would ask you ship it to my personal residence @ <REDACTED>, Toronto ON <REDACTED> (in the same region as tor01 datacenter). If you asked, I would come pick up the hard drive right now to help expedite this recovery! It's been over 24 hours that we have been offline and I am trying to help your team and their time back and forth with this courier. I can courier it back to your facility within 10 business days so you may claim it's warranty. Please let me know what works best. For me, I prefer to pick the drive up as soon as possible. The matter is critical. Thank you kindly,

Melaan Mahalingam   2021-05-11 12:06:15

Hello, I am one of the Site Manager's for the Toronto Region and this has been brought to my attention by Kevin. Looking through the ticket it seems the same issue occurred as per \[Update 49\] and this odd behavior is seems to occur once we connect HDD3 using the usb/sata cable. We are currently opening a Lenovo case to get this hardware fault checked out by them and the team is currently building out another server to match your current specifications. After physically verifying we see that the server is unresponsive and is in an "off" state. As we await Lenovo to do there investigation we will try a hard reboot of your host <pve1> to try and get the system back up. We will provide more information on your last \[Update 104\] regarding the drive being shipped. Thanks, Melaan M. Interim Site Manager IBM Cloud

Is this response helpful?

haieda.r***.com  2021-05-11 12:12:33

Hello, For update 104 In regards to having the device shipped out please allow me to provide that information to the Customer Success Manager (CSM) on the account and i will provide you with some updates in 20 mins. As we understand this is business critical we will do our best to get you this information as promptly as possible, once again thank you for your cooperation. Regards, Haieda R. Datacenter Tech, IBM Cloud

kevin.s***.com   2021-05-11 12:29:15

Hello, The hard reboot was successful and we have booted your server back into its operating system. The following are the current pings of host pve1: Management: Pinging 10.167.85.197 with 32 bytes of data: Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Private: Pinging 10.167.85.243 with 32 bytes of data: Request timed out. Request timed out. Public: Pinging 169.55.170.67 with 32 bytes of data: Reply from 169.55.170.67: bytes=32 time=1ms TTL=60 Reply from 169.55.170.67: bytes=32 time=1ms TTL=60 Attached is a screen shot of host pve1 in its operating system. We will update you again once we have finished creating a case for Lenovo to investigate. If you have any further inquiries please contact us. Thank you for your patience, Kevin S. Datacenter Technician IBM Cloud

kevin.s***.com   2021-05-11 12:29:44

File(s) attached to ticket OS CAP.PNG

haieda.r***.com  2021-05-11 12:50:24

Hello, We have created the case with Lenovo IBM problem number FNSWZL8, Once we get some updates in regards to the BMC issue we will update you promptly. we are now sending this ticket over to our Sales Team to assist on the Drive purchase process, they will update you shortly. Thank you, Haieda R. Datacenter Tech, IBM Cloud

HUNTER H***   2021-05-11 13:08:56

Hello, My name is Sunter and I will be assisting you with this hard drive purchase. Please provide the following information below: Customer Name: Customer Mailing Address: Hard Drive Requested: \*\*\*I have also attached a Drive Purchase Addendum that will need to be signed on your part and sent back. One I receive an update on this matter we can proceed as needed. Regards, Hunter H. Digital Inbound

Is this response helpful?

Jonathan Geller 2021-05-11 13:20:44

Hello Hunter- The drive is defective / faulty. This delivery is for data recovery efforts. Shipping and return only. However ADMIN fee is accepted. Customer Name: Jonathan Geller (SIPSTACK Inc.) Customer Mailing Address: (<REDACTED>) Hard Drive Requested: bthv6246008m800ogn (Faulty) Alternatively if the support team wishes to continue to attempt to access the drive, to advise. This courier method would probably be more cost effective for the IBM team. Please advise.

HUNTER H***   2021-05-11 13:27:21

Hello Jonathan, I am gaining information on the price of the drive before we can move further. If you are wishing to pick up the drive from the DC this is what is needed: "All hand pick-ups are to allow for 48 hours to gather all required approvals and prepare necessary documentation. Hand pick up must also occur during regular business hours (Monday-Friday 8:00am to 5:00PM). Before customer can pick up the drive(s) it they must go through the pre-approval process at the DC. On day of pick-up, the customer needs to provide photo ID, account ID, and ticket number corresponding to the drive(s) purchase request. Customer would sign document that confirms pick-up of asset." Do you wish to go this route? If so please provide the Name and contact information for you would be picking the drives up. Regards, Hunter H. Digital Inbound

Is this response helpful?

Jonathan Geller 2021-05-11 13:32:45

Yes I can pickup. name Jonathan Geller (<REDACTED>). Earliest time available. Please schedule a pickup and return for the hard drive 48 hours after initial 'hand pick-up'. Thank you kindly,

HUNTER H***   2021-05-11 13:45:25

Jonathan, I have attached the Drive Purchase Addendum. After further review I am now under the impression that you plan to return the drive. Unfortunately we do not take drives back and implement them. Once purchased and have left the facility, this drive is yours to do as you please, but not returnable. We will not ever take drives from outside of the DC to place into a server even if it is a drive purchased form IBM. My apologies for that misconception as I was not aware that you were looking to return the drive when complete. Do you still wish to proceed with this purchase? Regards, Hunter H. Digital Inbound

Is this response helpful?

Jonathan Geller 2021-05-11 13:51:50

Please provide the price for the defective drive. I will need to get approval from our board, legal and insurance. Thank you kindly,

Jonathan Geller 2021-05-11 16:48:33

Still awaiting a price....

HUNTER H***   2021-05-11 17:48:34

Hello Jonathan, In order for me to obtain pricing, I have to email our GTC team with the request for the drive. The expected turnaround from the start of a request to the completed all orders of operation for selling of a drive can take up to 48 hours. I expect to receive an update on pricing within 24 hours of the request being sent. I will update this case as soon as I receive the pricing information. Once I do receive this, I will need your approval as well as the form that was previously attached signed to move forward. Regards, Hunter H. Digital Inbound

Is this response helpful?

Jonathan Geller 2021-05-11 20:11:21

Please hand this back to support team. there is a server event that the systemboard failed. Server unresponsive, unable to turn on/off.

Rosario C***   2021-05-11 21:39:13

Hi Jonathan, I'm taking this ticket back to the DC team for now so we can look into your server being unresponsive. I'll update you in about 15-20 minutes. Regards, Rosario C Site Manager, TOR01 IBM Cloud

Is this response helpful?

Rosario C***   2021-05-11 21:49:05

Hi, I've confirmed what you mentioned and attached a screenshot showing the active event found through the XClarity Controller. We have already opened up a case with the vendor, Lenovo, to find out more details about what could be causing this. Something I would like to try immediately though is to disconnect the USB/SATA adapter that is currently connected to HDD3. Since it seems these 'SysBrd Vol Fault' errors started after we connected that device on the previous server, and the error on the new server showed up again after reconnecting it - we'll disconnect it now and see what happens. We'll also pull power from the server to get it booted up again once we disconnect the USB/SATA adapter. I'll provide an update in 15 minutes. Regards, Rosario C Site Manager, TOR01 IBM Cloud

Is this response helpful?

tenzin.w***.com  2021-05-11 22:34:37

Hello, This is the courtesy update that the server is not ping to private and public network: IPMI Network: Pinging 10.167.85.197 with 32 bytes of data: Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Private network: Pinging 10.167.85.243 with 32 bytes of data: Request timed out. Request timed out. Public Network: Pinging 169.55.170.67 with 32 bytes of data: Request timed out. Request timed out. Request timed out. Request timed out. Please standby for further update. Tenzin W*** Datacenter Technician IBM Cloud

tenzin.w***.com  2021-05-11 22:49:31

Hello, This is just a courtesy update that the server was on Operating System once disconnected the USB/SATA adapter. Please find the attached picture as a reference. Furthermore, we see an activity via crash cart that server was rebooted and accessing server BIOS setting. Regards, Tenzin W*** Datacenter Technician IBM Cloud

Jonathan Geller 2021-05-11 23:06:53

Any reason why the faulty drive was re-inserted into HDD3 slot as it is degraded and disabled. It was attached via USB for attempt in recovery, however at this time we would like to pick up the drive as discussed earlier in this thread.

Rosario C***   2021-05-11 23:15:18

Hi Jonathan, I saw that the arrangements to purchase/pick up the disk were still in progress so I thought in case there was anything else you may want to attempt to access the disk, it may be best to have it still connected. If you'd prefer, we can absolutely remove it and set it aside now. Thank you, Rosario C Site Manager, TOR01 IBM Cloud

Is this response helpful?

haieda.r***.com  2021-05-12 09:48:18

Hello, Just a quick monitoring update, we are closely monitoring all updates surrounding other concerns such as GTC pricing for the drive which we are waiting to hear back from we will keep you updated periodically: Server Pings: IPMI: PING 10.167.85.197 (10.167.85.197) 56(84) bytes of data. 64 bytes from 10.167.85.197: icmp\_seq=1 ttl=61 time=2.11 ms 64 bytes from 10.167.85.197: icmp\_seq=2 ttl=61 time=1.75 ms Eth0: PING 10.167.85.243 (10.167.85.243) 56(84) bytes of data. --- 10.167.85.243 ping statistics --- 4 packets transmitted, 0 received, 100% packet loss, time 3000ms Eth1: PING 169.55.170.67 (169.55.170.67) 56(84) bytes of data. 64 bytes from 169.55.170.67: icmp\_seq=1 ttl=60 time=0.972 ms 64 bytes from 169.55.170.67: icmp\_seq=2 ttl=60 time=0.965 ms Also attached below a screenshot of your servers OS for reference, More updates to follow. Thank you, Haieda R. Datacenter Tech, IBM Cloud

Jonathan Geller 2021-05-12 10:12:17

Thank you Haieda- While we wait for the defective drive pricing and time we can pickup, our legal and insurance team is asking if there is any other machine / service we can connect the damaged drive to, so we can remotely KVM to attempt recovery. Being 48 hours since the failure, we want to avoid further interruption.

Jonathan Geller 2021-05-12 10:14:04

Any bare metal with minimal specs to connect the sata drive (not on a RAID Controller) available hourly or daily? We could access within our existing VPN. Thank you kindly,

haieda.r***.com  2021-05-12 10:15:52

Hello Jonathan, Thank you for your prompt updates please give me a few mins to see if thats possible. I will update you again within 20 mins or less. Thank you, Haieda R. Datacenter Tech, IBM Cloud

haieda.r***.com  2021-05-12 10:34:14

Hello Jonathan, Thank you for your continued cooperation after reviewing your request in order for this to be possible you will have order another Bare Metal server for this case, we recommend something with the bare minimum Specs like the following: 1270V6 processor At least 2 drives 8GB RAM CentOS for the OS so that you have the storCli utility and the Provision time is lower. After the server has completed provisioning then we can add HDD3 to the server. Please let me know if you have any questions i will work with you to get them addressed. Thank you, Haieda R. Datacenter Tech, IBM Cloud

Jonathan Geller 2021-05-12 10:41:33

That is great news. Thank you kindly!

Jonathan Geller 2021-05-12 10:45:09

Will you be able to attach the drive without connecting to RAID controller?

haieda.r***.com  2021-05-12 10:49:18

Hello Jonathan, Please give me a moment to review your request and I will update you within 20 mins or less. Thank you, Haieda R. Datacenter Tech, IBM Cloud

haieda.r***.com  2021-05-12 10:54:17

Hello Jonathan, If you are looking to not have a RAID Controller for the new server you can order it as Onboard, also to touch upon the drives that you will order its best to order the same drives you have now as this server. Please let me know if you have any questions and we will be happy to assist you with them. Thank you, Haieda R. Datacenter Tech, IBM Cloud

Jonathan Geller 2021-05-12 11:34:00

Haieda- Server has been ordered #78567838. No OS required (especially speed is most important) , during KVM on BMC we can load recovery tools. Reminder, if the BMC reports device failure, it will be invisible to the OS. so hopefully when plugging into the 4th slot of the new server, no error will report. otherwise we will need SATA/USB connection. Thank you kindly,

haieda.r***.com  2021-05-12 11:39:06

Hello Jonathan, Thank you for the heads up im taking a look now i will update you again in 20 mins or less with updates. Please let me know if you have any questions and we will be happy to assist you with them. Thank you, Haieda R. Datacenter Tech, IBM Cloud

haieda.r***.com  2021-05-12 11:48:50

Hello Jonathan, After Reviewing the specification on the build we see that you ordered different drives from what you have in the host attached to this case, you also requested a RAID card but for clarity sake we understood that you did not want a RAID card: in the order we got: Processor: XEON-E3-1270-V3-Haswell 3.5 GHz RAM: DDR3-1333 Reg 32.0 GB Drive Controller: RAID CARD 4.0 Drives Hard Drive: SATAIII 1,000.0 GB Hard Drive: SATAIII 1,000.0 GB Hard Drive: SATAIII-SSD 960.0 GB Remote Mgmt Card: MGMT-KVM 1.0 Unit If this is correct please let us know, If however you intended different please list the specs here and we will match it to what you require. Please let me know if you have any questions and we will be happy to assist you with them and thank you for your cooperation. Regards, Haieda R. Datacenter Tech, IBM Cloud

Jonathan Geller 2021-05-12 11:52:07

Hi Haida- because hourly server was not available in tor01 region, I went with a server we would retain anyways. I requested that the faulty drive from pve1 server be connected directy via sata (or USB) if unable to bypass the BMC controller. the BMC may automaticlly disable the faulty drive, preventing the OS from seeing it. direct on SATA would be ideal for only the faulty drive. Hope this makes sense.

Jonathan Geller 2021-05-12 11:53:57

For clarity: I am not trying to boot from the faulty drive, only mount the partitions to a new OS.

haieda.r***.com  2021-05-12 11:54:31

Hi Jonathan, Thank you for the clarification let me review and i will update you again within 20 mins. Regards, Haieda R. Datacenter Tech, IBM Cloud

haieda.r***.com  2021-05-12 12:08:24

Hi Jonathan, Again thank you for the update, We are building the server now with the specs ordered and we will update you periodically with the progress as it goes through automation. Once the build is complete and gone through automation we will confirm with you when moving HDD3 from <pve1> to the new server so that you may be able to access it. Please let me know if you have any questions or concerns we will work with you to clear them up. Regards, Haieda R. Datacenter Tech, IBM Cloud

Jonathan Geller 2021-05-12 12:31:59

Is the new server not a Lenovo server?

haieda.r***.com  2021-05-12 12:33:57

Hi, No it is a SuperMicro, do you prefer it to be a Lenovo server? Regards, Haieda R. Datacenter Tech, IBM Cloud

Jonathan Geller 2021-05-12 12:35:14

Yes please. why we chose to partner with IBM.

haieda.r***.com  2021-05-12 12:37:27

Hi Jonathan, Thank you for your prompt update, please give me some time to address this and i will update you within 20 mins. Regards, Haieda R. Datacenter Tech, IBM Cloud

haieda.r***.com  2021-05-12 12:50:03

Hi Jonathan, Alright per your request we are now preparing a Lenovo server, we will update you again with progress. Regards, Haieda R. Datacenter Tech, IBM Cloud

haieda.r***.com  2021-05-12 13:25:02

Hi Jonathan, Thank you for your patience just to update you on the progress the server is now going through our automation system, we will update you periodically every hour with more progress update in regards to the status. Regards, Haieda R. Datacenter Tech, IBM Cloud

haieda.r***.com  2021-05-12 14:47:17

Hi Jonathan, The Server is still in the process of going through our automation system and is running smoothly. We will continue to update you periodically every hour with more progress update in regards to the status. Regards, Haieda R. Datacenter Tech, IBM Cloud

Jonathan Geller 2021-05-12 16:05:56

Can we connect the faulty drive into the new server? thank you kindly.

lavan.s***.com 2021-05-12 16:11:53

Hello Jonathan, Yes, we will commence the faulty drive transfer shortly. Further update is to follow within the next 20 minutes. Thanks, Lavan S. Datacenter Technician IBM CLOUD

lavan.s***.com 2021-05-12 16:46:09

Hello, We will commence taking out the faulty drive from host <pve1> after which the USB/SATA cable will then be attached scanned in HDD3 on host <pve02.tor01>. The following are pre-maintenance pings to show network connectivity for hosts: ---- HOST <pve1> MANAGEMENT: Pinging 10.167.85.197 Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 PRIVATE: Pinging 10.167.85.243 Request timed out. PUBLIC: Pinging 169.55.170.67 Reply from 169.55.170.67: bytes=32 time=1ms TTL=60 Reply from 169.55.170.67: bytes=32 time=1ms TTL=60 ========== HOST <pve02.tor01> MANAGEMENT: Pinging 10.167.85.203 Reply from 10.167.85.203: bytes=32 time=1ms TTL=61 Reply from 10.167.85.203: bytes=32 time=1ms TTL=61 PRIVATE: Pinging 10.167.85.213 Request timed out. PUBLIC: Pinging 169.55.170.69 Request timed out. Please standby for further update as we begin swapping faulty drive over to host <pve02.tor01> Thanks, Lavan S. Datacenter Technician IBM CLOUD

lavan.s***.com 2021-05-12 17:12:05

Hello, This is a courtesy update to inform you USB/SATA cable is attached to the scanned in HDD3 on host <pve02.tor01>. Please note network connectivity: HOST <pve02.tor01> MANAGEMENT: Pinging 10.167.85.203 Reply from 10.167.85.203: bytes=32 time=1ms TTL=61 Reply from 10.167.85.203: bytes=32 time=1ms TTL=61 PRIVATE: Pinging 10.167.85.213 Request timed out. PUBLIC: Pinging 169.55.170.69 Request timed out. Thanks, Lavan S. Datacenter Technician IBM CLOUD

Jonathan Geller 2021-05-13 00:40:17

OS installed on pve02. We do not have bios access, can you set primary boot device to: SLOT1:HD0 thank you kindly,

opeyemi.u***.com 2021-05-13 00:43:04

Hello, Kindly give us a moment to review your request, we will update you shortly. Regards, Opeyemi U. Data Center Technician IBM Cloud

opeyemi.u***.com 2021-05-13 00:57:13

Hello Jonathan, In order for us to set HDD0 as the boot device, we would have to gracefully shutdown your host < pve02> to make the necessary changes in BIOS. This can be done with your permission. We are on standby awaiting a response from you. Thank you for your understanding. Regards, Opeyemi U. Data Center Technician IBM Cloud

Jonathan Geller 2021-05-13 00:58:37

Sure. I've gone ahead and shutdown for you.

opeyemi.u***.com 2021-05-13 01:01:17

Hello Jonathan, Thank you for your update and permission. We will go ahead to carry out your request. Please standby. Regards, Opeyemi U. Data Center Technician IBM Cloud

opeyemi.u***.com 2021-05-13 01:08:18

Hello, We will now proceed to make the requested changes in BIOS, where we will make HDD0 the boot device of the host. Kinldy find pre maintenance pings below: Mgmt: PING 10.167.85.203 (10.167.85.203) 56(84) bytes of data. 64 bytes from 10.167.85.203: icmp\_seq=1 ttl=61 time=0.973 ms 64 bytes from 10.167.85.203: icmp\_seq=2 ttl=61 time=0.547 ms 64 bytes from 10.167.85.203: icmp\_seq=3 ttl=61 time=0.662 ms Eth0: PING 10.167.85.213 (10.167.85.213) 56(84) bytes of data. --- 10.167.85.213 ping statistics --- 3 packets transmitted, 0 received, 100% packet loss, time 1999ms Eth1: PING 169.55.170.69 (169.55.170.69) 56(84) bytes of data. --- 169.55.170.69 ping statistics --- 3 packets transmitted, 0 received, 100% packet loss, time 1999ms Please standby. Regards, Opeyemi U. Data Center Technician IBM Cloud

opeyemi.u***.com 2021-05-13 01:29:01

Hello, We have changed the boot device to HDD0 as requested and we have booted the host back up. Please confirm from your end that it is as expected. Kinldy find post maintenance pings below: Mgmt: PING 10.167.85.203 (10.167.85.203) 56(84) bytes of data. 64 bytes from 10.167.85.203: icmp\_seq=1 ttl=61 time=1.01 ms 64 bytes from 10.167.85.203: icmp\_seq=2 ttl=61 time=0.637 ms 64 bytes from 10.167.85.203: icmp\_seq=3 ttl=61 time=0.675 ms Eth0: PING 10.167.85.213 (10.167.85.213) 56(84) bytes of data. --- 10.167.85.213 ping statistics --- 3 packets transmitted, 0 received, 100% packet loss, time 1999ms Eth1: PING 169.55.170.69 (169.55.170.69) 56(84) bytes of data. --- 169.55.170.69 ping statistics --- 3 packets transmitted, 0 received, 100% packet loss, time 1999ms Regards, Opeyemi U. Data Center Technician IBM Cloud

Jonathan Geller 2021-05-13 01:30:28

Black screen on the KVM, no bootup.

Jonathan Geller 2021-05-13 01:30:55

when it does boot up, you will see eth1 return packets right away.

opeyemi.u***.com 2021-05-13 01:34:00

Hello, Give us a moment to review this. We will update you shortly. Regards, Opeyemi U. Data Center Technician IBM Cloud

opeyemi.u***.com 2021-05-13 01:39:44

Hello Jonathan, We see the screen as black screen as well. We will carry out a power cycle on the chassis in order for the server to reboot. We will continue to monitor the host till we receive ping packets on eth1. Please standby for further updates. Regards, Opeyemi U. Data Center Technician IBM Cloud

opeyemi.u***.com 2021-05-13 01:51:28

Hello Jonathan, We have tried a power cycle on the host and attempted to boot the server with HDD0 as the boot device. We still see a blank screen. Can you please verify from your end that the OS was installed properly on HDD0? Regards, Opeyemi U. Data Center Technician IBM Cloud

Jonathan Geller 2021-05-13 01:53:36

yes, and were able to boot to it after installation by pressing f12 and selecting the proper drive. see image attached.

Jonathan Geller 2021-05-13 01:57:37

The sidebar wont let me add the file. i think the maximum allowed has been reached on this thread.

Jonathan Geller 2021-05-13 02:02:37

I rebooted, and pressed f12 now, and selected HDD0 Slot 1, and is now online, and eth1 replying to pings... Please double check the boot order in bios is correct. Thank you kindly.

opeyemi.u***.com 2021-05-13 02:08:52

Hello, Thank you for your update. We will go ahead to carry out your request. Please standby for further updates. Regards, Opeyemi U. Data Center Technician IBM Cloud

opeyemi.u***.com 2021-05-13 02:24:19

Hello, We have verified that the boot order for the device and we can confirm that it is set to boot off of HDD0. We have attached a screenshot of your host in BIOS confirming the above statement. Please standby for further updates. Regards, Opeyemi U. Data Center Technician IBM Cloud

opeyemi.u***.com 2021-05-13 02:58:22

Hello, We have also selected the start option on the host as Hard Disk 0 in bios. We have provided a screenshot below for your reference. We will now transfer this ticket over to our support team to assist with the black screen seen on your host after it attempted to boot off of HDD0. Please standby for further updates. Regards, Opeyemi U. Data Center Technician IBM Cloud

ABRAHAM E*** 2021-05-13 03:15:52

Hello Jonathan, My name is Abraham and I will be assisting with this issue. Please could you provide on a .txt file the output of the command below? That will help us to check the health of all drives and proceed with the troubleshooting. Looking forward to hearing from you. /opt/lsi/storcli/storcli /c0 /dall showc0 /opt/lsi/storcli/storcli /c0 /vall show /opt/lsi/storcli/storcli /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir" /opt/lsi/storcli/storcli /c0 /eall /sall show all | grep -E '(Det|Cou|S\\.M|^SN)(?!.\*\\s(No|0)$)' /opt/lsi/storcli/storcli /c0 show eventloginfo /opt/lsi/storcli/storcli /c0 show all Thank you Abraham E. Compute Support Engineer IBM Cloud

Is this response helpful?

Jonathan Geller 2021-05-13 09:03:01

To be able to answer your question, I will need to KVM into pve2. However, while still connected to to the VPN, I am unable to access the the management interface on 10.167.85.203. Additionally I am unable to reach pve1 on 10.167.85.197. Has anything changed?

Jonathan Geller 2021-05-13 09:15:22

I am able to access both management consoles when I reverse tunnel into PVE1 public IP. Softlayer VPN will not let me ping or access either management console. While in PVE2 KVM, I rebooted, pressed f12 to select a drive, and server is now fully booted and public interface is responding to ping requests. Drive health is good as I am logged into the servers OS now. Here is an answer to your question after running the commands: root@pve02:~# /opt/lsi/storcli/storcli /c0 /dall showc0 -bash: /opt/lsi/storcli/storcli: No such file or directory root@pve02:~# /opt/lsi/storcli/storcli /c0 /vall show -bash: /opt/lsi/storcli/storcli: No such file or directory root@pve02:~# /opt/lsi/storcli/storcli /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir" -bash: /opt/lsi/storcli/storcli: No such file or directory root@pve02:~# /opt/lsi/storcli/storcli /c0 /eall /sall show all | grep -E '(Det|Cou|S\\.M|^SN)(?!.\*\\s(No|0)$)' -bash: /opt/lsi/storcli/storcli: No such file or directory root@pve02:~# /opt/lsi/storcli/storcli /c0 show eventloginfo -bash: /opt/lsi/storcli/storcli: No such file or directory root@pve02:~# /opt/lsi/storcli/storcli /c0 show all -bash: /opt/lsi/storcli/storcli: No such file or directory Please let me know when both the VPN is restored, as well as when our boot device can be set appropriately. I would also like to know why the softlayer VPN no longer works. I can see via my IAM user settings, VPN is enabled on the subnet.

Todd B***  2021-05-13 09:32:22

We will take a look at the boot device part of this here shortly. As for the VPN aspect, that will need to be looked into by another team. Please stand by Todd B Manager, Compute Support Engineers IBM Cloud Support

Is this response helpful?

ABRAHAM E*** 2021-05-13 10:53:30

Hi Jonathan, I am able to reach the user login prompt on the IPMI. but still unable to ping the private IP. Based on the traceroute command output the traffic might be blocked by an external security gateway. I will now transfer this case to our internal security for further investigation and will to you with another update ASAP Regards, Abraham E.

Is this response helpful?

Jonathan Geller 2021-05-13 10:54:53

before transfering, we need to resolve the server issues first. VPN is secondary.

Danny M*** 2021-05-13 12:39:53

Hello, After reviewing, it looks like your current issue is that you still need to press F12 during boot to select the correct drive. And then after this is resolved we will address your issues with the VPN and gateway. Please stand by as our support team assists. Danny M ACS Compute Support Lead IBM Cloud Support

Is this response helpful?

Jonathan Geller 2021-05-13 13:14:56

Thank you Danny- Feel free to power cycle the server as your team needs to. Nothing is live on PVE2 its a new server just activated.

Jonathan Geller 2021-05-13 14:41:13

Any updates so far?

Rosario C***   2021-05-13 14:44:10

Hi Jonathan, I see our ACS team is working with you on the newly ordered server. I'm just chiming in because we have just received pricing for the disk if you're still looking to purchase it. The disk with serial number: bthv6246008m800ogn and model SSDSC2BA800G401 will cost 549.95 USD. As this ticket has become quite long, we'll create a new one to track the purchase/transfer of the disk if you decide to move forward. Regards, Rosario C Site Manager, TOR01 IBM Cloud

Is this response helpful?

Jonathan Geller 2021-05-13 17:47:28

Thank you Rosario- transferring the hardware recovery to a new ticket is a good idea. When doing so, please provide what is required to make this happen fast, and what type of information you require from me for any security clearance. I should also mention that the new server we ordered yesterday PVE2 is till not operational / complete. Should the team be unable to finalize the order by 9pm tonight, I think it would be best to cancel the order.

Rosario C***   2021-05-13 18:24:52

Hi Jonathan, You're very welcome. I've created CS2306828 which has the information needed to move forward with getting the drive over to you and your team. Please take a look and let us know of any questions you have. Regards, Rosario C Site Manager, TOR01 IBM Cloud

Is this response helpful?

Jonathan Geller 2021-05-14 09:11:11

The new server pve02 still does not boot on its own to the first raid disk. only by pressing f12 and selecting. Please proceed to cancel the new server order #78567838

Jonathan Geller 2021-05-14 17:26:07

Is there any reason there has been no response to PVE02 new order still incomplete? Or that our VPN to our management consoles are also not working. This is a major risk. Please advise!

ssutherl***.com 2021-05-14 17:42:42

I cannot approve this ticket on behalf of Legal until the customer has signed and uploaded the Drive Purchase Addendum \[see update 110\].

Joshua L***  2021-05-15 20:28:15

Hello Jonathan, As our sales team mentioned, they are unable to approve the driver addition until you complete the requested actions. Let us know when you have filled out the requested forms or if you need anything else. Thank you, Joshua L Compute Support Engineer IBM Cloud cPanel & WHM Administrator Certification (CWA) cPanel & WHM System Administrator I Certification (CWSA-I)

Is this response helpful?

Jonathan Geller 2021-05-16 21:20:42

Hi Rosario- I have attached the addendum response for IBM legal in case# CS2306828. This thread will not allow me to upload any attachments anymore. Thank you kindly.

JESSE S***  2021-05-16 23:48:52

Hello, The case you referenced CS2306828 is with our hardware team, and they have forwarded the document to Legal. Please let us know if you need further assistance! Thank you, Jesse S Compute Support Engineer IBM Cloud IaaS

Is this response helpful?

Jonathan Geller 2021-05-18 12:05:05

Hello Shawn- I would like to request access to the damaged drive, via conference room @ tor01. I would be the person to handle and inspect the drive. Besides my personal information already provided, is there anything else required to schedule this visit? Thank you kindly.

Rosario C***   2021-05-18 12:47:14

Hi Jonathan, Apologies for the delay in response, this ticket is still with the ACS group. I'll take it back to our team's queue for now so that we can keep it monitored for further updates. I have your phone number, and email address from the info you already provided. Would I also be able to get a couple more pieces of information: -title position -date and time window you would like to be on site to access the drive Regards, Rosario C Site Manager, TOR01 IBM Cloud

Is this response helpful?

Jonathan Geller 2021-05-18 12:50:49

Hi Rosario- Position: CEO Time window: ~10amEST May 19 arrival Let me know if that works. Thank you kindly,

Rosario C***   2021-05-18 12:55:34

Hi, Thanks Jonathan. The request has been escalated up to DC Operations management and I'll provide you with more information as soon as possible. Regards, Rosario C Site Manager, TOR01 IBM Cloud

Is this response helpful?

Jonathan Geller 2021-05-18 13:34:44

Thanks Rosario - If you need broader window access, We could say arrival for 10pm EST May 19th, or 10am EST May 20th. Thank you kindly,

walter.t***.com  2021-05-18 13:45:51

Hello Jonathan, Thank you for your response. Please give us a moment, and we will update you again shortly. Sincerely, Walter T. Datacenter Technician IBM Cloud

Rosario C***   2021-05-19 08:29:08

Hi Jonathan, Can we go ahead and disconnect the failed drive? Regards, Rosario C Site Manager, TOR01 IBM Cloud

Is this response helpful?

Jonathan Geller 2021-05-19 11:00:42

Hi Rosario- To confirm from our conversation, that this would be confirmed once Pierre arrives onsite and ready to move damaged drive to the original server so that we can remotely monitor via KVM / management console. Thank you kindly,

Rosario C***   2021-05-19 11:08:28

Hi Jonathan, Thanks for the confirmation. We'll update you once we have new info to pass on. Regards, Rosario C Site Manager, TOR01 IBM Cloud

Is this response helpful?

Rosario C***   2021-05-19 11:29:57

Hi Jonathan, We're ready to move the drive over to pve1 now. Just as a final reminder, pve1 will undergo reboots and changes in settings as the work is being carried out. Let us know if you have any questions. Regards, Rosario C Site Manager, TOR01 IBM Cloud

Is this response helpful?

Jonathan Geller 2021-05-19 11:33:27

Thank you Rosario- please proceed. I have PVE1 KVM open as well.

Rosario C***   2021-05-19 11:37:36

Hi Jonathan, Thanks, I'll update you in a bit once we're done moving the disk over to pve1. Regards, Rosario C Site Manager, TOR01 IBM Cloud

Is this response helpful?

Rosario C***   2021-05-19 11:48:03

Hi Jonathan, The drive has been moved over to the empty slot in pve1 (HDD3). I'm informing Pierre as well. Thank you, Rosario C Site Manager, TOR01 IBM Cloud

Is this response helpful?

Pierre C***    2021-05-19 12:38:23

Hi Jonathan, We're going to power down <pve1> as you've mentioned that there is no production work on this server and have migrated work off of this host. For your information, we'll be doing the following just for verification purposes to confirm what was shown above in update 74: - Check System/RAID Bios information - Pull RAID logs - Attempt to force the drive online There will likely be several reboots, after this is complete, we'll return the server back to the OS. Ping pre-checks: MGMT - Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Private - Request timed out. Public - Reply from 169.55.170.67: bytes=32 time=1ms TTL=60 Regards, Pierre C*** Regional Lead, Mexico Canada Brazil

Is this response helpful?

Jonathan Geller 2021-05-19 12:40:27

Thank you Pierre- I'll continue to monitor from my end on the KVM.

kevin.s***.com   2021-05-19 12:53:19

Hello, You are very welcome. We will keep you updated as we proceed. If you have any questions feel free to let us know. Thank you, Kevin S. Datacenter Technician IBM Cloud

Pierre C***    2021-05-19 14:11:50

Hi Jonathan, The drive detects and is able to get serial information, but immediately gets set to a unconfigured bad state by the controller with the drive showing up as 0 capacity. This means that we are unable to troubleshoot the device any further, we did attempt a disk force online and to try to set the drive to raw passthrough to at least see if it would appear, but those attempts failed. I've attached a screenshot, your server is back online and pinging in the same state as before. MGMT - Reply from 10.167.85.197: bytes=32 time=2ms TTL=61 Private - Request timed out. Public - Reply from 169.55.170.67: bytes=32 time=2ms TTL=61 Regards, Pierre C*** Regional Lead, Mexico Canada Brazil

Is this response helpful?

System  2021-06-03 18:34:18

Close notes: Case was in a Waiting state for longer than 7 days, Case was automatically resolved

System  2021-06-03 18:34:18

Case was in a Waiting state for longer than 7 days, Case was automatically resolved

John B***  2021-06-11 19:41:16

Case was in a Resolved state for longer than 7 days, Case was automatically closed

Is this response helpful?