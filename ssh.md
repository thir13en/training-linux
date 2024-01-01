# SSH

## Connect to a remote
```bash
$ ssh <ip-addr>
```
or
```bash
$ ssh -l <ip-addr>
```
`-l` is the flag to specify username.

## Obtain ip address of Linux machine
```bash
ifcong
```
You might need to have installed the `net-tools` package. The ip will be found in the `inet` containing line.