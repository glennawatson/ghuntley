---
title: Git
layout: notes
---

# signed commits

## on a new machine

1. install keybase and gpg4win


If I do have access to my yubikey:

```
keybase pgp export | gpg --import
```

If I don't have access to my yubikey:

```
keybase pgp export -q 13DAEF2E995C1055A87C0AB71E0F156E39D1D3A6 --secret | gpg --import --allow-secret-key-import
```


## configuration

```
[credential]
	helper = manager
[filter "lfs"]
	clean = git-lfs clean -- %f
	smudge = git-lfs smudge -- %f
	process = git-lfs filter-process
	required = true
[gpg]
	program = c:\\Program Files (x86)\\GnuPG\\bin\\gpg.exe
[commit]
	gpgsign = true
[user]
	signingkey = 13DAEF2E995C1055A87C0AB71E0F156E39D1D3A6
	email = ghuntley@ghuntley.com
	name = Geoffrey Huntley
```

## reference material
- https://ttmm.io/tech/yubikey/
- https://blog.scottlowe.org/2017/09/06/using-keybase-gpg-macos/


# Shallow clones
fast clones without the history

`git clone $repo --depth=1`


{{<
tweet 1033084211605979137 >}} 
