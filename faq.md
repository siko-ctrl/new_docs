---
description: FREQUENTLY ASKED QUESTIONS
---

# ❓ FAQs & Troubleshooting

<details>

<summary>what is JSON-RPC?</summary>

A Noso Remote Procedure Call (RPC) node is a type server that allows users to read data on the Noso blockchain and manipulate it for various purposes. Full details [here](https://docs.nosocoin.com/noso-developers-portal/rpc-connection/running-a-noso-rpc-node-for-development) (for exchanges)

</details>

<details>

<summary><strong>Why is noso.exe flagged as a virus?</strong></summary>

In the last decade or so, the anti-virus software began using a method called heuristics to better detect viruses that had code to evade detection. While that helped with a better detection, it also came with the undesirable side effect of false positives. This happens more often with non-signed software that has code to access the Internet. Since both, the wallet and the earning app do access the Internet, they trigger a false positive. They do not have a virus, they just tickle the anti-virus software the wrong way.

</details>

<details>

<summary><strong>Is Noso listed at any Exchange?</strong></summary>

Currently Noso is listed on [Txbit.io](https://www.txbit.io/Trade/NOSO/USDT)

</details>

<details>

<summary><strong>How do I create a new wallet address?</strong></summary>

This can be done from inside any of the Noso Wallets. From within Nosolite, right click under <mark style="color:red;">**“Address”**</mark>, select <mark style="color:red;">**“New.”**</mark> From within Noso Mobile or Noso Web Wallets, select the <mark style="color:red;">**“New”**</mark> button on the top left under the Noso logo. For Noso Wallet, select the <mark style="color:red;">**“+”**</mark> button to the right of the <mark style="color:red;">**“Address”**</mark> header. <mark style="color:green;">**Remember to backup your wallet every time you create a new wallet address**</mark>**.**

</details>

<details>

<summary>Why is NosoNode is displaying "block undone" over-and-over, not showing a satellite dish, and not paying?</summary>

For various reasons, NosoNode can get into a stuck state. Use the command **"**<mark style="color:green;">**reqsum**</mark>**"** to restore the node to a functional state.

</details>

<details>

<summary>`GLIBC_2.34' not found  when running nosonode how to fix it?</summary>

**Under releases on github you will see multiple mirrors "**<mark style="color:green;">**linuxnew**</mark>**" corresponds to newer releases like Ubuntu 22.04**\
&#x20;**"**<mark style="color:green;">**linux**</mark>**" corresponds to older releases like Ubuntu 20,Ubuntu 18**

</details>

<details>

<summary>SSL files missed <mark style="color:blue;"><strong>on windows</strong></mark>. Auto directive update will not work properly if nosonode shows this please use this step</summary>

Upload these ssl files to your noso directory to fix( the .dll files  [https://github.com/Noso-Project/NosoNode/tree/main/ssl](https://github.com/Noso-Project/NosoNode/tree/main/ssl)

</details>

<details>

<summary>SSL files missed <mark style="color:green;"><strong>on Linux</strong></mark>. Auto directive update will not work properly if nosonode shows this please use this step</summary>

Use this command in terminal <mark style="color:red;">**sudo apt-get install libssl-dev**</mark>

</details>
