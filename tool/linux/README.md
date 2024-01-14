---
description: Learn how to install CrackMapExec on Linux machines.
cover: ../../.gitbook/assets/GitBook Covers (1).png
coverY: 0
---

# 🟢 Linux

### Install from repository

If you are using Kali you can install it from Kali repos but I recommend you to install it from git source.

```
apt install crackmapexec
```

### Install some Dependencies

```
apt-get install -y libssl-dev libffi-dev python-dev-is-python3 build-essential
```

### Install from Git Hub

```bash
git clone --recursive https://github.com/byt3bl33d3r/CrackMapExec
cd CrackMapExec
poetry install
#poetry run crackmapexec
```
