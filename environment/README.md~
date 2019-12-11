The mainnet fullnode has a file structure as below:

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

### File contents:

1. [genesis.json](genesis.json)
2. [swagger.json](../capabilities/swagger.json) use OAS2 [swagger editor](https://editor.swagger.io) to explore.
3. agreement.cdv - ???
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
 

### genesis directory

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


### Database - [sqlite](https://www.sqlite.org)

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



