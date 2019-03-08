---
title: PicoCTF 2017 - computeAES
date: 2018-07-05
layout: post
tags: [PicoCTF, CTF, Writeups]
---

# computeAES

> Encrypted with AES in ECB mode. All values base64 encoded
> 
> ciphertext = t1h0qbcOhRQF5E46bsNLimfbcI6egrKP4LHtKR3lT4UdWjhssM8RQSBT7S/8rcRy
>
> key = T5uVzYtuBNv6vwjohslV4w==

Base64 to Hex Converter => https://cryptii.com/base64-to-hex

AES Decrypter => http://aes.online-domain-tools.com/

Convert ciphertext (base64) to hex =>
```markdown
b7 58 74 a9 b7 0e 85 14 05 e4 4e 3a 6e c3 4b 8a 67 db 70 8e 9e 82 b2 8f e0 b1 ed 29 1d e5 4f 85 1d 5a 38 6c b0 cf 11 41 20 53 ed 2f fc ad c4 72
```

Convert key (base64) to hex =>

```markdown
4f 9b 95 cd 8b 6e 04 db fa bf 08 e8 86 c9 55 e3
```

Use online tool to solve;

```markdown
f	l	a	g	{	d	o	_	n	o	t	_	l	e	t	_
m	a	c	h	i	n	e	s	_	w	i	n	_	1	e	6
b	4	c	f	4	}	_	_	_	_	_	_	_	_	_	_
```

`do_not_let_machines_win_1e6b4cf4`