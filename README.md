Measured GPU Speeds:
- V100 - 728 MH/s default, 7094 MH/s upgraded
- P100 - ? MH/s default, ? MH/s upgraded
- GTX1080 - 300 MH/s default, 2950 MH/s upgraded 
- GTX1080Ti - ? MH/s default, ? MH/s upgraded
- GTX1050 - ? MH/s default, ? MH/s upgraded
- K80 - ? MH/s default, ? MH/s upgraded

Dependencies :
- Ubuntu 16.04
- [CUDA 8.0 or later](https://askubuntu.com/a/799185)
```
sudo apt-get install gpg erlang libncurses5-dev libssl-dev unixodbc-dev g++ git
sudo apt-get install build-essential
sudo apt-get install curl
```

Setup [Only needed for the first time]:
1. Set Pubkey in miner_gpu.erl
2. Set [mining pool address](https://github.com/decryptoed/amoveo-cuda-miner/blob/master/docs/pools.md) in miner_gpu.erl if necessary.
3. [Tune the parameters of your GPU](https://github.com/decryptoed/amoveo-cuda-miner/blob/master/docs/tuning.md).

Steps to mine:
1. sh start_miner.sh ([Multi-GPU Instructions](https://github.com/decryptoed/amoveo-cuda-miner/blob/master/docs/Multi-GPU.md))
2. To see debug info, open debug.txt ("tail -f debug0.txt" in a separate terminal to stream debug info)
3. sh clean.sh when finished mining

Steps to perform perf test
1. sh perftest.sh

By default, the miner will mine to [Mandel Hoff's mining pool](http://amoveopool.com/) that takes a 3% fee with shared payouts.

The CUDA code here is a basic and unoptimized version for Amoveo GPU mining. An upgrade is available to provide the most optimized CUDA code for Amoveo GPU mining, and typically gives a 3-8x performance improvement, depending on your GPU. For upgrade inquiries, please contact decryptoed@gmail.com or @Iridescence in the Amoveo telegram.

Donations to encourage improvements and optimizations:

Amoveo - BIGGeST9w6M//7Bo8iLnqFSrLLnkDXHj9WFFc+kwxeWm2FBBi0NDS0ERROgBiNQqv47wkh0iABPN1/2ECooCTOM=

Bitcoin - 39RMFMprjdzCRvedLhFdz5uNEzTP4uMbkV

Ethereum - 0x74ed96b787def62e9b183ff5fc0e93753ebc4c76