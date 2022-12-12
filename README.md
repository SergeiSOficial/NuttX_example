# NuttX_example
NuttX RTOS example with LVGL


Environment windows 11 WSL2 Ubuntu

[Part 1]
Init Code
```
sudo apt-get update
sudo apt install -y unzip gcc-arm-none-eabi binutils-arm-none-eabi kconfig-frontends bison flex gettext texinfo \
libncurses5-dev libncursesw5-dev gperf automake libtool pkg-config build-essential gperf genromfs libgmp-dev\
 libmpc-dev libmpfr-dev libisl-dev binutils-dev libelf-dev libexpat-dev gcc-multilib g++-multilib picocom \
 u-boot-tools util-linux openocd
https://github.com/SergeiSOficial/NuttX_example nuttxspace
cd nuttxspace
git clone 
git submodule add https://github.com/apache/nuttx.git nuttx
git submodule add https://github.com/apache/nuttx-apps apps
cd nuttx
./tools/configure.sh -l sim:lvgl_lcd
make -j24
./nuttx
```
![](img/Screenshot%202022-12-10%20123604.jpg)

To run on STM32F746
```
make distclean
make clean
./tools/configure.sh -l stm32f746g-disco:lvgl
make -j24
```


```
./tools/configure.sh -a ../myapp -l sim:lvgl_lcd
```