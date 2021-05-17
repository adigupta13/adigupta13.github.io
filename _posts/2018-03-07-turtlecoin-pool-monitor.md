---
layout: post
title: "TRTL Mining Pool Observer"
icon: fas fa-server
---

![turtlecoin]({{site.baseurl}}/images/pool_monitor/trtl.jpg)

[Turtlecoin](https://turtlecoin.lol/) is a small community driven project, aimed at creating a privacy centric low fees cryptocurrency. This project is also compared as similar alternative to [Dogecoin](https://dogecoin.com/).

Like many other cryptocurrencies, Turtlecoin employs the Proof-of-Work {PoW} mechanism to arrive at consensus for each block. Originally created as method to thwart denial of service attacks, PoW quickly became one of the most widely used mechanisms in public blockchains.

Miners deploy their computing power to take part in the block generation process. The network assigns a problem to the nodes (miners) on the network. The miner who computes the problem and submits the result at the earliest wins the block reward. The time to generate this result varies based on the computing power a miner has and random hash it starts computing from.

![mining]({{site.baseurl}}/images/pool_monitor/mining.jpg)

As the number of miners in a network increases, miners start realizing less frequent block awards for their work, especially in an immensely popular network like bitcoin, where there can be millions of participants, competing for the next block. This is where mining pools comes into play.

To get more block rewards, miners often choose to club their individual comput units into one larger computing infrastructure having a capacity the sum of all its constituents. This pool of computers, mining pool now gets a better chance at receiving awards in a timely fashion which are then paid out to its participants proportional to their comtributed computing power.

Mining pools for turtlecoin are based on the same concept. As a miner in one of the pools, I felt the need to keep constant track of my desktop's mining progress though out the day while I was away from my desk. While remoting into the machine was a viable solution, it was definitely not the most elegant one. So I started to look for alternatives and found none, and then I decided to fix this problem myself.

I quickly realised that most if not all mining pools used [CryptoNote](https://github.com/fancoder/cryptonote-universal-pool) forks to build their solutions. While some of them did have a web UI to display mining statistics to user, many did not. But helpfully cryptonote did expose an endpoint where I could query mining statistics for a particular address. This also meant that now I could interface to all mining pools on turtlecoin. After some discussions with turtlecoin creators, I was able to design and develop and android app that showed realtime statistics like active workers, unpaid balances, average hashrates etc.

> Mission accomplished!

![screenshot_app]({{site.baseurl}}/images/pool_monitor/screenshot.png)

The application was officially recognised and featured on the turtlecoin website and [blog](https://medium.com/@turtlecoin/this-week-in-turtlecoin-feb-24-2018-873ba23acafe).

### Updates 08/09/2020

The application has been taken down by PlayStore as it violates it's policies for being affiliated to cryptocurrency mining. The application still lives on [mirrors](https://www.apkmonk.com/app/ml.fifty9.poolmonitor/)

[![repo](https://opengraph.githubassets.com/ce8fa1d42610c32aa920cc07d32f17ff7701400444504fe5522163f0f70948bf/adigupta13/TRTLMiningPoolObserver)](https://github.com/adigupta13/TRTLMiningPoolObserver)
