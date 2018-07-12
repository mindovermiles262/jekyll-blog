---
title: PicoCTF 2017 - Digital Camouflage
date: 2018-07-05
layout: post
tags: PicoCTF Kali
---

Open `data.pcap` in Wireshark

Search for `http.request.method == "POST"` to find TCP Stream
    Right Click > Follow > TCP Stream
    
Find `userid` and `pswrd` in stream:

```bash
userid=mathewsr&pswrd=aHJLUVNTTFd2Rw%3D%3D
```

From which we can extract the password:

```bash
pswrd=aHJLUVNTTFd2Rw==
```

The two `==` at the end tell us it's a base64-encoded cipher. We can decrpt using the command line:

```bash
echo aHJLUVNTTFd2Rw== | base64 --decode
hrKQSSLWvG
```

Copy and paste the password to get your 50 points