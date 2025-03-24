# cl-mem

cl-mem is an OpenCL memory benchmark utility.

Version 0.2 tests sequential write and read speeds.
Version 0.3 added sequential copy.
Random read/write tests are planned for a later version.

example R9 380 with memory clocked at 1.5Ghz:

    Running write test.
    128 GB in 1150.1 ms (111.3 GB/s)
    Running read test.
    128 GB in 779.5 ms (164.2 GB/s)
    Running copy test.
    128 GB in 906.2 ms (141.3 GB/s)

## Benchmarking CPU+GPU on CIX systems:

```bash
sudo apt update
sudo apt install -y build-essential git lmbench opencl-headers
git clone https://github.com/RadxaYuntian/cl-mem-cix.git
cd cl-mem-cix
make
/usr/lib/lmbench/bin/bw_mem -P 10 -N 2 1024M rd & ./cl-mem
```

# Thanks

cl-mem uses code from Marc Bevand's SILENTARMY zcash miner
