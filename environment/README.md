### Code base

[goal] is the command line tool and is install in `/usr/bin/goal`.
The algod daemon is controlled by the *algorand service( that starts
automatically on image launch, defaults to a DATADIR of
/var/lib/algorand.  Uses
[systemctl](http://manpages.ubuntu.com/manpages/bionic/man1/systemctl.1.html)
to start, stop or check status of algorand service.

```bash
algorand  1448  9.3  2.0 1350988 83084 ?       Ssl  14:53   2:39 /usr/bin/algod -d /var/lib/algorand
```

[Source code github repo](https://github.com/algorand/go-algorand)

```bash
$ls -l go-algorand

-rw-rw-r--  1 ubuntu ubuntu  4420 Dec 11 15:33 CONTRIBUTING.md
-rw-rw-r--  1 ubuntu ubuntu 36469 Dec 11 15:33 COPYING
-rw-rw-r--  1 ubuntu ubuntu  3099 Dec 11 15:33 COPYING_FAQ
-rw-rw-r--  1 ubuntu ubuntu  8415 Dec 11 15:33 Makefile
-rw-rw-r--  1 ubuntu ubuntu  7821 Dec 11 15:33 README.md
-rw-rw-r--  1 ubuntu ubuntu   235 Dec 11 15:33 THANKS.md
drwxrwxr-x  5 ubuntu ubuntu  4096 Dec 11 15:33 agreement
drwxrwxr-x  3 ubuntu ubuntu  4096 Dec 11 15:33 auction
drwxrwxr-x  2 ubuntu ubuntu  4096 Dec 11 15:33 catchup
drwxrwxr-x 29 ubuntu ubuntu  4096 Dec 11 15:33 cmd
drwxrwxr-x  3 ubuntu ubuntu  4096 Dec 11 15:33 components
drwxrwxr-x  2 ubuntu ubuntu  4096 Dec 11 15:33 config
drwxrwxr-x  6 ubuntu ubuntu  4096 Dec 11 15:33 crypto
drwxrwxr-x  4 ubuntu ubuntu  4096 Dec 11 15:33 daemon
drwxrwxr-x 10 ubuntu ubuntu  4096 Dec 11 15:33 data
drwxrwxr-x  5 ubuntu ubuntu  4096 Dec 11 15:33 debug
drwxrwxr-x  5 ubuntu ubuntu  4096 Dec 11 15:33 docker
drwxrwxr-x  2 ubuntu ubuntu  4096 Dec 11 15:33 docs
drwxrwxr-x  3 ubuntu ubuntu  4096 Dec 11 15:33 gen
-rw-rw-r--  1 ubuntu ubuntu  2416 Dec 11 15:33 go.mod
-rw-rw-r--  1 ubuntu ubuntu 13534 Dec 11 15:33 go.sum
drwxrwxr-x  6 ubuntu ubuntu  4096 Dec 11 15:33 installer
drwxrwxr-x  2 ubuntu ubuntu  4096 Dec 11 15:33 ledger
drwxrwxr-x  2 ubuntu ubuntu  4096 Dec 11 15:33 libgoal
drwxrwxr-x  4 ubuntu ubuntu  4096 Dec 11 15:33 logging
drwxrwxr-x  3 ubuntu ubuntu  4096 Dec 11 15:33 netdeploy
drwxrwxr-x  2 ubuntu ubuntu  4096 Dec 11 15:33 network
drwxrwxr-x  3 ubuntu ubuntu  4096 Dec 11 15:33 node
drwxrwxr-x  2 ubuntu ubuntu  4096 Dec 11 15:33 nodecontrol
drwxrwxr-x  2 ubuntu ubuntu  4096 Dec 11 15:33 protocol
drwxrwxr-x  2 ubuntu ubuntu  4096 Dec 11 15:33 rpcs
drwxrwxr-x  7 ubuntu ubuntu  4096 Dec 11 15:33 scripts
drwxrwxr-x  4 ubuntu ubuntu  4096 Dec 11 15:33 shared
drwxrwxr-x  8 ubuntu ubuntu  4096 Dec 11 15:33 test
drwxrwxr-x  4 ubuntu ubuntu  4096 Dec 11 15:33 tools
drwxrwxr-x 12 ubuntu ubuntu  4096 Dec 11 15:33 util
drwxrwxr-x  3 ubuntu ubuntu  4096 Dec 11 15:33 wallet
```


### File structure

```bash
$ls -l /var/lib/algorand

-rw-r--r-- 1 algorand algorand  472129968 Dec 11 14:56 agreement.cdv
-rw-r--r-- 1 algorand algorand 1073742491 Dec 11 10:21 agreement.cdv.archive
-rw------- 1 algorand algorand          0 Nov 29 21:28 algod.lock
-rw-r--r-- 1 algorand algorand         15 Dec 11 14:53 algod.net
-rw-r--r-- 1 algorand algorand          5 Dec 11 14:53 algod.pid
-rw-r--r-- 1 algorand algorand         64 Nov 29 21:28 algod.token
-rw-r--r-- 1 algorand algorand       1632 Nov 29 21:26 config.json
drwxrwxr-x 6 algorand algorand         65 Nov 29 21:24 genesis
-rw-r--r-- 1 algorand algorand      24972 Nov 22 16:20 genesis.json
drwx------ 2 algorand algorand        332 Dec 11 14:53 mainnet-v1.0
-rw-r--r-- 1 algorand algorand 1073741338 Dec  4 09:07 node.archive.log
-rw-r--r-- 1 algorand algorand  741449011 Dec 11 14:56 node.log
-rw-r--r-- 1 algorand algorand         23 Nov 22 16:20 system.json
```

### File contents

1. [genesis.json](genesis.json)
2. [swagger.json](../capabilities/swagger.json) use OAS2 [swagger editor](https://editor.swagger.io) to explore.
3. [agreement.cdv](https://github.com/algorand/go-algorand/blob/master/agreement/README.md) - consensus protocol implementation 
4. agreement.cdv.archive - previous version of agrrement.cdv
5. algod.
   * lock - internal use
   * net - hostname:port, default 127.0.0.1:8080
   * pid - linux process id for algorand deamon
   * token - security token
6. [config.json](../configurations/default.json)
7. node.archive.log - ??
8. node.log - node log file
9. system.json - ```json {"shared_server":true}```
 

### Genesis directory

```bash
drwxrwxr-x 2 algorand algorand 26 Nov 29 21:24 betanet
drwxrwxr-x 2 algorand algorand 26 Nov 29 21:24 devnet
drwxrwxr-x 2 algorand algorand 26 Nov 29 21:24 mainnet
drwxrwxr-x 2 algorand algorand 26 Nov 29 21:24 testnet

genesis/betanet:
-rw-r--r-- 1 algorand algorand 8859 Nov 22 16:20 genesis.json
genesis/devnet:
-rw-r--r-- 1 algorand algorand 8859 Nov 22 16:20 genesis.json
genesis/mainnet:
-rw-r--r-- 1 algorand algorand 24972 Nov 22 16:20 genesis.json
genesis/testnet:
-rw-r--r-- 1 algorand algorand 34754 Nov 22 16:20 genesis.json
```

### Database - [sqlite](https://www.sqlite.org)

```bash
$ sudo ls -l $CHAIN_DATA/mainnet-v1.0/

-rw-r--r-- 1 algorand algorand        4096 Nov 29 21:28 crash.sqlite
-rw-r--r-- 1 algorand algorand       32768 Dec 11 14:53 crash.sqlite-shm
-rw-r--r-- 1 algorand algorand        8272 Nov 29 21:28 crash.sqlite-wal
-rw-r--r-- 1 algorand algorand   331816960 Dec 11 14:55 indexer.sqlite
-rw-r--r-- 1 algorand algorand       32768 Dec 11 14:57 indexer.sqlite-shm
-rw-r--r-- 1 algorand algorand     4152992 Dec 11 14:57 indexer.sqlite-wal
-rw-r--r-- 1 algorand algorand 54579613696 Dec 11 14:55 ledger.block.sqlite
-rw-r--r-- 1 algorand algorand       32768 Dec 11 14:57 ledger.block.sqlite-shm
-rw-r--r-- 1 algorand algorand     4280712 Dec 11 14:57 ledger.block.sqlite-wal
-rw-r--r-- 1 algorand algorand     3207168 Dec 11 14:54 ledger.tracker.sqlite
-rw-r--r-- 1 algorand algorand       32768 Dec 11 14:57 ledger.tracker.sqlite-shm
-rw-r--r-- 1 algorand algorand     4602072 Dec 11 14:57 ledger.tracker.sqlite-wal
```

### Footprint

The `algod` daemon has a minimal footprint when executing, typically consuming 7% CPU and 2% memory (of 4Gb) when sync'd.


```bash
top - 15:25:43 up 33 min,  1 user,  load average: 0.03, 0.03, 0.07
Tasks: 108 total,   1 running,  58 sleeping,   0 stopped,   0 zombie
%Cpu(s):  2.7 us,  0.0 sy,  0.0 ni, 97.1 id,  0.0 wa,  0.0 hi,  0.0 si,  0.2 st
KiB Mem :  4038260 total,  3052696 free,   186896 used,   798668 buff/cache
KiB Swap:        0 total,        0 free,        0 used.  3632164 avail Mem 

  PID USER      PR  NI    VIRT    RES    SHR S  %CPU %MEM     TIME+ COMMAND    
 1448 algorand  20   0 1350988  83196  19820 S   7.3  2.1   2:52.10 algod      
    1 root      20   0  159648   8992   6788 S   0.0  0.2   0:02.76 systemd    

...
```
  