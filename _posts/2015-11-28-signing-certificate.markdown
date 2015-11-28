---
layout: post
title:  "signing certificate"
date:   2015-11-28 14:44:38
categories: jekyll update
---

```
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout private.key -out private.crt
```

