# Pluto_fw
Record the progress of designing the synchronization IP of pluto SDR

### Environment
Os: Ubuntu 22.04Lte <br>
Tools: Vivado 2021.1 <br>
       Matlab R2021a <br>
While installing Vivado at Linux we need the packets below:
``` python
  sudo apt-get update
  sudo apt-get upgrade
  sudo apt-get install libncurses5
  sudo apt-get install libtinfo5
  sudo apt-get install libncurses5-dev libncursesw5-dev
  sudo apt-get install ncurses-compat-libs
```
We need command below to launch Vivado:
``` python
  sudo su
  source /tools/Xilinx/Vivado/2021.1/settings64.sh
  vivado

```
According to https://wiki.analog.com/university/tools/pluto/building_the_image, we have something to verify.

Depending on the version of Xilinx tools, you need to make sure that you have the 32-bit libraries (the Xilinx tools are distributed as 32-bit binaries).
```
find /tools/Xilinx/ -name vivado -executable -type f | xargs file | grep ELF
ELF 64-bit LSB executable, x86-64, version 1 (GNU/Linux), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 2.6.32, stripped

```
This specifies any shell prompt running on your Linux development host

```
sudo apt-get install git build-essential ccache device-tree-compiler dfu-util fakeroot help2man libncurses5-dev libssl1.0-dev mtools rsync u-boot-tools bc python cpio zip unzip file wget

```
We use Alphan's design (https://github.com/alphansahin/Wireless-Federated-Learning-with-Non-coherent-Over-the-Air-Computation) for our start-up foundation for Time Synchronization.

Start a new project, choose the default part as below.
![image](https://github.com/ZhihanX/Pluto_fw/assets/114545801/e61685c8-5f09-42af-8eec-e20b9086c391)

