# job_data_2023


## Compute Node Specifications

```
$ sacct -M traverse -a -X -P -n -S 2023-01-01T00:00:00 -E 2023-12-31T23:59:59 -o user,cluster,start,end,ncpus,nnodes,alloctres,nodelist
```

#### Traverse

CPU:

```
jdh4@traverse-k05g9:~$ lscpu
Architecture:        ppc64le
Byte Order:          Little Endian
CPU(s):              128
On-line CPU(s) list: 0-127
Thread(s) per core:  4
Core(s) per socket:  16
Socket(s):           2
NUMA node(s):        6
Model:               2.3 (pvr 004e 1203)
Model name:          POWER9, altivec supported
CPU max MHz:         3800.0000
CPU min MHz:         2300.0000
L1d cache:           32K
L1i cache:           32K
L2 cache:            512K
L3 cache:            10240K
NUMA node0 CPU(s):   0-63
NUMA node8 CPU(s):   64-127
NUMA node252 CPU(s): 
NUMA node253 CPU(s): 
NUMA node254 CPU(s): 
NUMA node255 CPU(s): 
```

Note that there are 4 hardware threads per CPU-core. Each node has 2 sockets with 16 CPU-cores per sockets giving 128 hardware threads. Several codes run optimally using on 1 hardware thread per CPU-core.

Total CPU memory per node is 250 GB.

GPU:

```
Tesla V100-SXM2-32GB
```
