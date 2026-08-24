# Netstat
it's a network command used to debug ports, processes and reachability
```bash
netstat -tlupn
```
**Note:** `netstat -tlupn` is a Linux command that shows listening TCP and UDP network sockets, along with the processes using them. <br>

1. -t — show TCP sockets <br>
2. -l — show listening sockets <br>
3. -u — show UDP sockets <br>
4. -p — show the PID and program name using each socket <br>
5. -n — show numeric addresses/ports instead of resolving hostnames/services <br>