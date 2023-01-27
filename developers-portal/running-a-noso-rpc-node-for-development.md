---
description: >-
  A Noso Remote Procedure Call (RPC) node is a type server that allows users to
  read data on the Noso blockchain and manipulate it for various purposes.
---

# Running A Noso RPC node for development

The Noso RPC node enables the front-end application layer and the backend protocol layer to interact with one another through a request-reply function that transmits information between the client and server.

\
To set up a Noso RPC node, you must first download and install NosoNode software from the Noso Project Github repository (here) [https://github.com/Noso-Project/NosoNode](https://github.com/Noso-Project/NosoNode). Once NosoNode software is installed, navigate to the “Options > RPC” tab. From the RPC tab, specify your RPC TCP port (Default 8078) and check the box “Enable JSON-RPC server”. You will see the word RPC in yellow at the bottom indicating RPC is enabled. It is highly recommended to whitelist the IP addresses of specific servers allowed to connect especially when hosted publicly.

\


<figure><img src="https://lh5.googleusercontent.com/nl0FyDUzIF4wPXs6hSoRTYUI52FEu37HmVwtSzt4toBCu5yHEXPGbw__4GBwleEfmrn9XQL4kqILwXbUzMr5RCN3XP93nRRmHVh9VI8P2hgHmoC9I9MX6eZy9TPw3w1CacYzf5Orl5SQ8X6_ZclsL-f_8CxZE8sfzEeqMIdZsGlDWhaORvMZuiLuFVwvuA" alt=""><figcaption><p>The following JSON Remote Procedure Calls are accessible</p></figcaption></figure>



\
<mark style="color:red;">**“getorderinfo”**</mark> returns: timestamp, block, receiver, amount, reference of the specified order.

{% hint style="info" %}
Example JSON-RPC call:&#x20;

{ "jsonrpc" : "2.0", "method" : "getaddressbalance", "params" : \["NpryectdevepmentfundsGE"], "id" : 7 }

Example JSON-RPC Result:

{ "jsonrpc" : "2.0", "result" : \[{ "valid" : true, "address" : "NpryectdevepmentfundsGE", "alias" : null, "balance" : 3350262539961, "incoming" : 0, "outgoing" : 0 }], "id" : 7 }
{% endhint %}



<mark style="color:red;">**“getblockinfo”**</mark> returns: number, timestart, timeend, timetotal, last20, totaltransactions, difficulty,target, solution, lastblockhash, nextdifficulty, miner, feespayed, reward of the specified block.

{% hint style="info" %}
Example JSON-RPC call:

{ "jsonrpc" : "2.0", "method" : "getblocksinfo", "params" : \["94490"], "id" : 9 }

Example JSON-RPC Result:

{ "jsonrpc" : "2.0", "result" : \[{ "valid" : true, "number" : 94490, "timestart" : 1674790801, "timeend" : 1674791400, "timetotal" : 599, "last20" : 0, "totaltransactions" : 29, "difficulty" : 0, "target" : "154F217AD7EF6D07E689C608802DB1F1", "solution" : "!!5!!!!!!!!!!!!!!!10146144900000010166482959134325258D04D0B245009535120500795820",&#x20;

"lastblockhash" : "154F217AD7EF6D07E689C608802DB1F1", "nextdifficult" : 193, "miner" : "N2MVecGnXGHpN8z4RqwJFXSQP6doVDv", "feespaid" : 194370, "reward" : 5000000000, "hash" : "5E71D00A2945E0884893ACD9A0C6AD72" }], "id" : 9 }
{% endhint %}

\
<mark style="color:red;">**“getpendingorders”**</mark> returns: a list of pending orders.

{% hint style="info" %}
Example JSON-RPC call:

{ "jsonrpc" : "2.0", "method" : "getpendingorders", "params" : \[], "id" : 14 }

Example JSON-RPC Result:

{ "jsonrpc" : "2.0", "result" : \[{ "pendings" : \["TRFR,N2MVecGnXGHpN8z4RqwJFXSQP6doVDv,N4KmPqzkYdeZYneAxtjLQCoZyUhDpHT,111807580,11181", "TRFR,N3pzgU2jpvhjW6cSJL8zW8Rzj5fJdFa,Nfk2RJQG7xTUdR8TckhgtrqRLPyGEx,31472638,3147", "TRFR,N3ESwXxCAR4jw3GVHgmKiX9zx1ojWEf,N2BhUYhiepHVke8V7NVrUdit42xnAEt,76848009,7685", "TRFR,N3aXz2RGwj8LAZgtgyyXNRkfQ1EMnFC,N2kWBgQHrtiQPASTK67WmvtoL8e5GDn,55644228,5564", "TRFR,N2MVecGnXGHpN8z4RqwJFXSQP6doVDv,N2kWBgQHrtiQPASTK67WmvtoL8e5GDn,112276488,11228", "TRFR,N2MVecGnXGHpN8z4RqwJFXSQP6doVDv,N48ZtdfyydBDRVopeSxveQ2qCpWa9GL,9800480,980", "TRFR,N3ESwXxCAR4jw3GVHgmKiX9zx1ojWEf,NEsMdywQNHXWpMnoxNhtsGREyW9GGE,77904269,7791", "TRFR,N3pzgU2jpvhjW6cSJL8zW8Rzj5fJdFa,N7U1brSR8RBqrZZGMRhZQ8KP8MPNC1,103411950,10342", "TRFR,N3aXz2RGwj8LAZgtgyyXNRkfQ1EMnFC,Ntgp6CmSLVUzLrxVD2z21Ve7r2M5DR,46803208,4680", "TRFR,N2ophUoAzJw9LtgXbYMiB4u5jWWGJF7,N3TSJcSz9wetKamQUcjHUGsCtnkuCGB,99340774,9935", "TRFR,N2MVecGnXGHpN8z4RqwJFXSQP6doVDv,N3ZMRpo2c6xaJyTUNTeqbFbVZtui3Fb,103614686,10362", "TRFR,N3ESwXxCAR4jw3GVHgmKiX9zx1ojWEf,N2kWBgQHrtiQPASTK67WmvtoL8e5GDn,77904269,7791"] }], "id" : 14 }
{% endhint %}



“getmainnetinfo” returns: lastblock, lastblockhash, headershash, summaryhash, pending, supply.

{% hint style="info" %}
**Example** JSON-RPC call:

{ "jsonrpc" : "2.0", "method" : "getmainnetinfo", "params" : \[], "id" : 15 }

Example JSON-RPC Result:

{ "jsonrpc" : "2.0", "result" : \[{ "lastblock" : 94490, "lastblockhash" : "5E71D00A2945E0884893ACD9A0C6AD72", "headershash" : "E41D37527B0A9F0A01C63F32C52562E9", "sumaryhash" : "C21483546A23510F65E36FE0781B6FF7", "pending" : 12, "supply" : 473480390730000 }], "id" : 15 }
{% endhint %}



\




\


\
\


\


***

\
