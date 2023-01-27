# 💰 Earn Noso using a Mobile Device:

<mark style="color:red;">To earn Noso Coins, you will need a wallet and "Noso Earn" software</mark>\
\
**Step 1:**\
Download and install the latest version of NosoMobile wallet from Github.com [(here)](https://github.com/Noso-Project/NosoWallet-Android/releases).\
\
\
![Noso Mobile Wallet](https://nosocoin.com/docs/images/nosomobile.png)\
\
\
Upon installation, wallet will generate a default address that you will need to copy/paste in a later step.\
\
**Step 2:**\
Install the Termux App from FDroid app store [(here)](https://f-droid.org/F-Droid.apk) **NOT from Google Playstore!** Once FDroid is installed, open FDroid and Install Termux.\
\
**Step 3:**\
Launch Termux App and perform the following:

1-Update Termux: `pkg update`\


2-Upgrade Termux: `pkg upgrade`\


3-Install Proot Distro: `pkg install proot-distro`\


4-Install Debian: `proot-distro install debian`\


5-Login to Debian: `proot-distro login debian`\


6-Now that you are logged into Proot-Distro Debian, Update, upgrade and install wget and nano:\
&#x20;`apt-get update -y && apt-get upgrade -y && apt-get install wget -y && apt-get install nano -y`

7-Download "Get Noso" app for your architecture. If you are unsure, type `uname -m` to determine 32bit or 64bit.\
Download "Get Noso" app (version 1.6). Check [(here)](https://github.com/Noso-Project/noso-website/tree/main/docs/download) for other versions. wget:\
&#x20;`wget https://nosocoin.com/docs/download/consominer2-v1.6-aarch64-linux`(aarch64)\
\


```
wget https://nosocoin.com/docs/download/consominer2-v1.6-arm32-linux(arm32)
```

\


8-Make "Get Noso" app executable:\
&#x20;`chmod +x consominer2-v1.6-aarch64-linux`(aarch64)\
`chmod +x consominer2-v1.6-arm32-linux`(arm32)

**Step 4:**\
Run "Get Noso" app from within Termux/proot-Distro/Debian: \
`./consominer2-v1.6-aarch64-linux`(aarch64)\
`./consominer2-v1.6-arm32-linux`(arm32)\
The inital run creates files needed for further configuration.\
\
**Step5:**\
Close "Get Noso" app with the key combination `alt+X`\
Once closed, you will need to edit the consominer2.cfg configuration file\
Make sure "consominer2.cfg" exists by typing `ls` You should see files similar to the following:\
\
![directory listing](https://nosocoin.com/docs/images/termux\_ls.jpg) \
Use nano to edit the consominer2.cfg:`nano consominer2.cfg`\
Update, copy/paste your wallet address into configuration, set your CPU, and test to "false"\
\
SEE IMAGE BELOW:\
\
![consominer2 config](https://nosocoin.com/docs/images/consominercfg.png)\
\
Close and save your changes using the key combination `CTRL+X` and when prompted type `Y` to save changes.\
\
With configurations in place, you are now ready to start earning coins.\
\
Please note, a typical earning period consists of **48 blocks** from the moment you start participating. It takes 7 1/2 hours to go through 48 blocks and you will not see coins in your wallet until after the 7 1/2 hours has lapsed. When participating, you will see a "balance" column with coins pending in green. This is the balance of coins you will receive when your participation period has expired.\
\
![](https://nosocoin.com/docs/images/consominerbal.png)\
\


If you have issues with using Termux with Proot Distro on your device, try Userland following instructions [(here).](userland-instructions.md)

\
