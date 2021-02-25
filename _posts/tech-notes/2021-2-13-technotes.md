---
title: "Tech Notes: ideas that are forgotten"
date: 2021-2-28 10:00:00 +07:00
tags: [software]
description: hello edwin
---

set git hub to use ssh

```bash
ssh-keygen -t ed25519 -C "zamudio.e13@gmail.com" 
ssh-add ~/.ssh/id_ed25519 
xclip -selection clipboard < ~/.ssh/id_ed25519.pub #add clip to github keys
# for repositories that use https
git remote set-url origin git@github.com:user/repo.git
```

Python range does not include the end .-.