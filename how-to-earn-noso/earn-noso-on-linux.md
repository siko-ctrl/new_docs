# 💰 Earn Noso on Linux

{% hint style="warning" %}
<mark style="color:red;">To earn Noso, you need a wallet and "Noso Earn" software</mark>
{% endhint %}

\
**Step 1:**\
Download the and install latest version of Nosolite wallet for your OS from Github.com [(here)](https://github.com/Noso-Project/NosoLite/releases)\
Upon installation, Nosolite will generate a default address to use for earning and holding Noso coins.\
\
**Step 2:**\
Download and install the latest "Get Noso"software from Github.com [(here)](https://github.com/Noso-Project/consominer2/releases)

From within a terminal on your Linux machine, enter the following commands:

* <mark style="color:red;">**`sudo apt-get update -y && apt-get upgrade -y`**</mark>
* <mark style="color:red;">**`wget`**</mark> [<mark style="color:red;">**`https://github.com/Noso-Project/nosoearn/releases/download/v2.3/nosoearn-v2.3-x86_64-ubuntu-latest.tar.gz`**</mark>](https://github.com/Noso-Project/nosoearn/releases/download/v2.3/nosoearn-v2.3-x86\_64-ubuntu-latest.tar.gz)\

* <mark style="color:red;">**`tar -xvzf`**</mark> [<mark style="color:red;">**`nosoearn-v2.3-x86_64-ubuntu-latest.tar.gz`**</mark>](https://github.com/Noso-Project/nosoearn/releases/download/v2.3/nosoearn-v2.3-x86\_64-ubuntu-latest.tar.gz)\

* <mark style="color:red;">**`chmod +x`**</mark> [<mark style="color:red;">**`nosoearn-v2.3-x86_64-ubuntu-latest`**</mark>](https://github.com/Noso-Project/nosoearn/releases/download/v2.3/nosoearn-v2.3-x86\_64-ubuntu-latest.tar.gz)\

* <mark style="color:red;">**`./`**</mark>[<mark style="color:red;">**`nosoearn-v2.3-x86_64-ubuntu-latest`**</mark>](https://github.com/Noso-Project/nosoearn/releases/download/v2.3/nosoearn-v2.3-x86\_64-ubuntu-latest.tar.gz)

{% hint style="danger" %}
Note, these  assume x86 64bit hardware. If your system has an arm or aarch64 CPU, you will need to use a different binary. Refer to Earn Noso on a Mobile Device for your ARM binary download.

<mark style="color:red;">**ALSO please notice that if your linux version is Ubuntu 20 and bellow you will need to the run the mirror version**</mark>
{% endhint %}

\
**Step 3:**\
After launching "Get Noso" software, press <mark style="color:red;">`ALT+X`</mark> to close. The first "run" will auto-create your configuration files.\
\
Open "nosoearn.cfg" using a text editor like Nano. <mark style="color:red;">`nano nosoearn.cfg`</mark>\
Select an address from your NosoLite wallet and modify your nosoearn.cfg file by modifying the following fields:\


* <mark style="color:red;">`address AddressFromYourNosoLiteWallet`</mark>
* <mark style="color:red;">`test`</mark> False (set this to "False" so that Earning starts as soon as the app opens)
* <mark style="color:red;">`custom seed`</mark>(change "mypasswrd" to a secure password which is 8-16 Base58 chars length)
* Close Nano and save your changes using the key combination `CTRL+X` and when prompted type `Y` to save changes.

With configurations in place, you are now ready to start earning coins.\


{% hint style="info" %}
Please note, a typical earning period consists of **48 blocks** from the moment you start participating. It takes 7 1/2 hours to go through 48 blocks and you will not see coins in your wallet until after the 7 1/2 hours has lapsed. When participating, you will see a "balance" column with coins pending in green. This is the balance of coins you will receive when your participation period has expired.
{% endhint %}

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

## <mark style="color:yellow;">Happy Earning!!!</mark>
