#### gssh

simple command line to utility to run commands on multiple hosts in parallel

##### Usage

```
echo host1 > /tmp/hosts
echo host2 >> /tmp/hosts
gssh -f /tmp/hosts uname -a

host1:stdout:Linux host1 2.6.32-431.11.2.el6.x86_64 #1 SMP Tue Mar 25 19:59:55 UTC 2014 x86_64 x86_64 x86_64 GNU/Linux
host2:stdout:Linux host2 2.6.32-431.11.2.el6.x86_64 #1 SMP Tue Mar 25 19:59:55 UTC 2014 x86_64 x86_64 x86_64 GNU/Linux
```

```
gssh -r host1..2 uname -a
```

###### Overriding ssh options

Example:

```
gssh -f file -- -o ConnectTimeout=30 -o BatchMode=yes id
```

##### Installation

1. Install go
2. go get -u -v github.com/square/gssh
