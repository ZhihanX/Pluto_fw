# Pluto_fw
Record the progress of designing the synchronization IP of pluto SDR

### Environment
Os: Ubuntu 22.04Lte
Tools: Vivado 2021.1
       Matlab R2021a
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

We use Alphan's design (https://github.com/alphansahin/Wireless-Federated-Learning-with-Non-coherent-Over-the-Air-Computation) for our start-up foundation for Time Synchronization.
