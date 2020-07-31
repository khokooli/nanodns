# Nano DNS ### Simple Dns Server In Go
Simple and tiny DNS server written in Golang for filtering domains and speed up name resolution functionality.  
Core features:  
forward and cache dns queries  
block domain names with regex.  

### Installation 
Prerequisites: [Golang](https://golang.org) + [Git](https://git-scm.com)  
Installing for windows - linux - freebsd and macos. (linux is recommended)  
Clone the code form Github or Snix servers.
```
# git clone https://snix.ir/snix/nanodns.git  # Snix
# https://github.com/khokooli/nanodns.git     # Github  
# cd nanodns 
# go get -v
# go build .
# ./nanodns
2020/07/31 05:11:29 upstream dns: 1.1.1.1:53 connection udp
2020/07/31 05:11:29 dns listen on: 0.0.0.0:53 connection udp
2020/07/31 05:11:29 load banned domains from: noacc.txt

```

### Usage and Options
```
# ./nanodns -h
Usage of ./dns-server:
  -fakeadd string
        an ip to send back for filtered domains <ipaddr> (default "127.0.0.1")
  -filter string
        filtered domains <filename> - regex is supported (default "noacc.txt")
  -loaddr string
        dns server listen address <ipaddr:port> (default "0.0.0.0:53")
  -loconn string
        dns server connection type <udp|tcp> (default "udp")
  -upaddr string
        upsteam dns server to connect <ipaddr:port> (default "1.1.1.1:53")
  -upconn string
        upsteam dns connection type <udp|tcp> (default "udp")
```

### Regex Domain Blocking
You can use regex for blocking domain names, create a file like `noacc.txt` in `nanodns` directory.   
For blocking all `com` and `example.net` put the following in `noacc.txt`  
[Regex Test Online](https://www.regextester.com/)  
```
^([a-z0-9]+[.])*com.$
example.net.

```

### Support and Social Media
So if you interested to learn [Golang](https://golang.org) follow my [Instagram Account](https://instagram.com/Gonoobies), Thanks. 
