# everything-Quantum
 
## Setup Cuda
https://docs.nvidia.com/cuda/cuda-installation-guide-linux/#post-installation-actions
## INstall drivers (for Nvidia 1660TI 550 is working with "nvidia-smi")
https://www.nvidia.com/en-us/drivers/details/241089/

n(base) quantum-machine@Quantum-Machine:~$ nvidia-smi
Sat Mar  8 11:38:43 2025
+-----------------------------------------------------------------------------------------+
| NVIDIA-SMI 550.144.03             Driver Version: 550.144.03     CUDA Version: 12.4     |
|-----------------------------------------+------------------------+----------------------+
| GPU  Name                 Persistence-M | Bus-Id          Disp.A | Volatile Uncorr. ECC |
| Fan  Temp   Perf          Pwr:Usage/Cap |           Memory-Usage | GPU-Util  Compute M. |
|                                         |                        |               MIG M. |
|=========================================+========================+======================|
|   0  NVIDIA GeForce GTX 1660 ...    Off |   00000000:01:00.0 Off |                  N/A |
| N/A   41C    P8              3W /   30W |       9MiB /   6144MiB |      0%      Default |
|                                         |                        |                  N/A |
+-----------------------------------------+------------------------+----------------------+
                                                                                         
+-----------------------------------------------------------------------------------------+
| Processes:                                                                              |
|  GPU   GI   CI        PID   Type   Process name                              GPU Memory |
|        ID   ID                                                               Usage      |
|=========================================================================================|
|    0   N/A  N/A      3693      G   /usr/lib/xorg/Xorg                              4MiB |
|    0   N/A  N/A     32462      G   /usr/bin/nvidia-settings                        1MiB |
+-----------------------------------------------------------------------------------------+

## Use Nvidia container toolkit setup
https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html

## Then use NVCR.io to  install required Container (make sure to use correcet architecture)

sudo docker run --gpus all --ipc=host --ulimit memlock=-1 --ulimit stack=67108864 -it --rm nvcr.io/nvidia/tensorflow:25.02-tf2-py3

# Enjoy!!!!!!! 
