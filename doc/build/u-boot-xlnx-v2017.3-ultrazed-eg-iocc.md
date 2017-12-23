### Build U-Boot

#### Download U-Boot Source

##### Clone from u-boot-xlnx.git

```
shell$ git clone https://github.com/Xilinx/linux-xlnx.git u-boot-xlnx-v2017.3-ultrazed-eg-iocc
```

##### Checkout xilinx-v2017.3

```
shell$ cd u-boot-xlnx-v2017.3-ultrazed-eg-iocc
shell$ git checkout -b xilinx-v2017.3-ultrazed-eg-iocc refs/tags/xilinx-v2017.3
```

#### Patch for UltraZed-EG-IOCC

```
shell$ patch -p0 < ../files/u-boot-2016.03-zynq-zybo.diff
shell$ git add --update
shell$ git commit -m "patch for UltraZed-EG-IOCC"
```

#### Setup for Build 

```
shell$ cd u-boot-xlnx-v2017.3-ultrazed-eg-iocc
shell$ export ARCH=arm
shell$ export CROSS_COMPILE=aarch64-linux-gnu-
shell$ make xilinx_zynqmp_uz3eg_iocc_defconfig
```

#### Build u-boot

```
shell$ make
```
