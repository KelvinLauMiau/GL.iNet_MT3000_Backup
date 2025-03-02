# GL.iNet_MT3000_Backup
Backup Files for GL.iNet's MT3000 plugins include iStoreOS, Argon, SSR.

## ATTENTION
* This project and all its content are for personal backup use only, and no liability will be assumed for any consequences.
* If you find this project useful, please give me a star, thank you.

## Flash firmware through UBOOT

MT3000 factory firmware can be downloaded here. First, download the firmware to your computer:
https://fw.gl-inet.cn/firmware/mt3000/release/openwrt-mt3000-4.7.0-1205-1733363917.img.

Then, use an Ethernet cable to connect the LAN port of the router to the computer. Hold the reset button, and after the indicator light flashes blue 6 times, release the button when the white light turns on.

Next, go to Windows Control Panel >> Network and Sharing Center >> Ethernet >> Properties >> Internet Protocol Version 4 (TCP/IPv4).

![image](https://github.com/user-attachments/assets/a6bb1252-ba2d-47ae-9fd9-3786c7acc9f9)

Set the IP to 192.168.1.2, set the subnet mask to 255.255.255.0, then confirm three times and plug and unplug the Ethernet cable. Then, access "http://192.168.1.1" using Google Chrome, then see

![image](https://github.com/user-attachments/assets/2f41cac6-0ef9-471f-82ff-e9207a1e76a0)

Here, choose 'File', then click 'Update'. The upload takes approximately 5 minutes, so it is recommended to wait a bit longer.

![image](https://github.com/user-attachments/assets/28925a64-a940-41fe-b7e9-71ae88971611)

Generally speaking, if the following appears, the upload is already complete, or confirm that the Wi-Fi is already detectable.

![image](https://github.com/user-attachments/assets/98e9f38f-e315-444c-b82e-7ff065bb0c91)

Continue below, change the previous IP to automatic.

![image](https://github.com/user-attachments/assets/c4bdfbbf-d249-4484-8178-514a45425b24)

Then plug and unplug the network cable, go to http://192.168.8.1, then configure the administrator password and network name, and so on.

![image](https://github.com/user-attachments/assets/78e03b96-9658-423c-a930-fef0949bc438)

## Configure LuCI

Go to System >> Advanced Settings >> Go to LuCI.
![image](https://github.com/user-attachments/assets/7daf147a-3f46-4753-adcb-fcc7076842f9)

Go to System >> Software Packages >> Find Configure opkg...

![image](https://github.com/user-attachments/assets/8e2949d5-6391-49c3-b758-bba6db5de0f8)

Then see this, and insert the link in the middle: 'src/gz dllkids https://op.dllkids.xyz/packages/aarch64_cortex-a53'. Note the spaces. Don't forget to update list.

![image](https://github.com/user-attachments/assets/d8328f03-bfea-44be-8670-e2a2d02e420b)

Find the file luci-theme-argon-master_2.2.9.4_all.ipk, choose Upload Package, and proceed with the installation. After installation, select System >> System >> Language and Interface, and confirm the interface as Argon.

![image](https://github.com/user-attachments/assets/9656a0c2-55e1-4cd8-8626-b1ae2822927e)

Go to the Argon page, then go to System >> Software Packages, upload the package, and find https://istore.linkease.com/repo/all/store/taskd_1.0.3-1_all.ipk, or the provided one, and install it first.

![image](https://github.com/user-attachments/assets/b08a81a9-6a41-47f1-9c69-27cfa9a85aaa)

Using a similar method, install luci-lib-xterm_4.18.0_all.ipk, luci-lib-taskd_1.0.18_all.ipk, and luci-app-store_0.1.14-1_all.ipk. It is crucial to follow the order.

![image](https://github.com/user-attachments/assets/f4379e87-541b-431d-94d0-95e86777763e)

## Configure iStore

Now we can see
![image](https://github.com/user-attachments/assets/590cedcb-e10c-458b-b8ce-d66a344c9342)

Then Manually install the provided SSR or OpenClash, checkout the provided .run files in iStoreOS, or find your own one.

![image](https://github.com/user-attachments/assets/b05ed2f6-fea5-4d4f-bb1e-ecdf5e97c95d)

Once finished, it is complete as long as a green box is displayed

![image](https://github.com/user-attachments/assets/32af358e-674f-4574-a427-0790fcf1c158)

Afterwards, you can insert your SS/SSR/V2Ray/Clash links on your own, no instruction needed at all.

![image](https://github.com/user-attachments/assets/05ab51ad-c8e3-4e59-9184-962a7b17b09b)

Usually it works properly.

![image](https://github.com/user-attachments/assets/366cf716-2346-49f3-988d-1f45418d65ee)

We end here, please use legally and exercise self-respect. If you have seen this, kindly give me a star, thank you.
