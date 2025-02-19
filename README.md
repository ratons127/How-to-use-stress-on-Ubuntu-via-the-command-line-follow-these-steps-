# How-to-use-stress-on-Ubuntu-via-the-command-line-follow-these-steps-
To use stress on Ubuntu via the command line, follow these steps:

###  Install stress
```
sudo apt install stress
```
### Use tmux for multiple termnal
```
sudo apt install tmux
```
```
tumx
```
ctrl + B, % , arrow keys 
<br>
<br>

###  Basic Usage
>Stress the CPU
To stress test the CPU (using 4 worker threads, you can adjust the number of threads based on your CPU cores):

```
stress --cpu 4
```
This command will cause the CPU to work at full capacity. You can specify the number of workers to match the number of CPU cores on your machine for a more intense test.
<br>
<br>

### Stress the Memory
```
stress --vm 2 --vm-bytes 1G
```
This will use 2 worker threads to allocate 1 GB of memory per worker.

<br>
<br>

### Stress the I/O
You can also stress the I/O subsystem with:
```
stress --io 4
```
This will spawn 4 threads that perform I/O operations, putting load on the disk.

<br>
<br>

### Specify Duration
If you want to run the stress test for a specific amount of time (e.g., 60 seconds):
```
stress --cpu 4 --timeout 60s
```
This will stress the CPU for 60 seconds.

###  Combining Multiple Tests
You can combine different types of stress tests:
```
stress --cpu 4 --io 2 --vm 2 --vm-bytes 1G --timeout 5m
```
This command will stress 4 CPU cores, 2 I/O threads, 2 memory workers (with 1GB of memory each), and will run for 5 minutes.

### Check System Load
While stress testing, you might want to check the system's resource usage:
```
top
```
```
htop
```
```
dstat
```
```
vmstat
```
Use top or htop to monitor CPU and memory usage.
Use dstat or vmstat to track real-time system performance.





















```
