################################################################################

1. How to Build
	- get Toolchain
		From android git server , codesourcery and etc ..
		 - arm-eabi-4.7
		
	- edit Makefile
		edit "CROSS_COMPILE" to right toolchain path(You downloaded).
		  EX)  export CROSS_COMPILE= $(android platform directory you download)/android/gcc/prebuilts/linux-x86/arm/arm-eabi-4.7/bin/arm-eabi-
       		  Ex)  export CROSS_COMPILE=/usr/local/toolchain/arm-eabi-4.7/bin/arm-eabi-          // check the location of toolchain

		$ export ARCH=arm
		$ make msm8974_sec_defconfig VARIANT_DEFCONFIG=msm8974pro_sec_klte_vzw_defconfig SELINUX_DEFCONFIG=selinux_defconfig
		$ make

2. Output filesS
	- Kernel : arch/arm/boot/zImage
	- module : drivers/*/*.ko

3. How to Clean	
		$ make clean
################################################################################
