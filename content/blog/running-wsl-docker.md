---
title: "WSL2 and Docker"
date: 2020-03-02T12:14:34+06:00
image: "https://res.cloudinary.com/aalbero/image/upload/v1597260175/raspberry-pi_zfsn48.svg"
description: "Running docker in windows home with WSL2"
author: "Alvaro Albero"
type: "post"
---
[See original post in my LinkedIn](https://www.linkedin.com/posts/alvaro-albero-gran-416554128_wsl2-docker-error-response-from-daemon-activity-6648048351952678912-5ZqN)

I was able to run Docker on Windows Home using WSL 2 and I'm quite happy about it because I had previously failed to use docker engine in windows as one of the requirements is to have the pro version.

The other day I read a bit about WSL 2 and decided to go ahead and install it, you need to get an insider version of Windows first but it's not a big deal. Then I saw the edge release of Docker desktop works in WSL 2 for windows home, and indeed it did.

At this point I was wondering, if the new WSL 2 has it's own Linux kernel, why cannot I install directly Docker as if it was a Linux machine? I went ahead and followed those steps. It did not work directly, but after following the steps in this Github issue https://lnkd.in/gXzqYWn, I was able to successfully run docker hello-world in my linux bash!

I am currently working in a blockchain project with Hyperledger Sawtooth and an easy way to implement a test node is by running a docker container. I am really excited to be able to do this in Windows!

#docker #WSL2

