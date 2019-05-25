---
title: Git
layout: notes
---

# signed commits

## on a new machine

install keybase and gpg4win

```
keybase pgp export | gpg --import
keybase pgp export -q 13DAEF2E995C1055A87C0AB71E0F156E39D1D3A6 --secret | gpg --import --allow-secret-key-import
```

# Shallow clones
fast clones without the history

`git clone $repo --depth=1`


{{<
tweet 1033084211605979137 >}} 
