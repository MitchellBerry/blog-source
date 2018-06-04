---
title: Golang Debian/Ubuntu Installation
date: 2017-09-15 10:18:21
tags: Go, Debian, Ubuntu
---

Quick bash script to install a specific Go version. 

```bash
#!/bin/bash
read -p "Enter Go version (e.g 1.7): " version
wget https://dl.google.com/go/go$version.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go$version.linux-amd64.tar.gz
rm go$version.linux-amd64.tar.gz
echo "export PATH=$PATH:/usr/local/go/bin" >> ~/.profile
export PATH=$PATH:/usr/local/go/bin
mkdir ~/go
echo "Version:"
go version
echo "GOPATH:"
go env GOPATH
```


