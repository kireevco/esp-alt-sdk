# ESP8266 Cross platform SDK
### Build Status:
##### xtensa-lx106-elf
| Windows | MacOS | Linux |
| ------- | ----- | ----- |
| [![Build Status](https://jenkins.dandle.co/buildStatus/icon?job=xtensa-lx106-elf/label=build-win2012r2x64-01)](https://jenkins.dandle.co/job/xtensa-lx106-elf/label=build-win2012r2x64-01/)| [![Build Status](https://jenkins.dandle.co/buildStatus/icon?job=xtensa-lx106-elf/label=build-osx-01)](https://jenkins.dandle.co/job/xtensa-lx106-elf/label=build-osx-01/) | [![Build Status](https://jenkins.dandle.co/buildStatus/icon?job=xtensa-lx106-elf/label=build-ubuntu14-01)](https://jenkins.dandle.co/job/xtensa-lx106-elf/label=build-ubuntu14-01/) |

##### esp-alt-sdk
| SDK | Windows | MacOS | Linux |
| ------------- | ------------- | ------------- | ------------- |
| 1.4.0 | [![Build Status](https://jenkins.dandle.co/buildStatus/icon?job=esp-alt-sdk/VERSION=1.4.0,label=build-win2012r2x64-01)](https://jenkins.dandle.co/job/esp-alt-sdk/VERSION=1.4.0,label=build-win2012r2x64-01/) | [![Build Status](https://jenkins.dandle.co/buildStatus/icon?job=esp-alt-sdk/VERSION=1.4.0,label=build-osx-01)](https://jenkins.dandle.co/job/esp-alt-sdk/VERSION=1.4.0,label=build-osx-01/) | [![Build Status](https://jenkins.dandle.co/buildStatus/icon?job=esp-alt-sdk/VERSION=1.4.0,label=build-ubuntu14-01)](https://jenkins.dandle.co/job/esp-alt-sdk/VERSION=1.4.0,label=build-ubuntu14-01) |
| 1.5.0 | [![Build Status](https://jenkins.dandle.co/buildStatus/icon?job=esp-alt-sdk/VERSION=1.5.0,label=build-win2012r2x64-01)](https://jenkins.dandle.co/job/esp-alt-sdk/VERSION=1.5.0,label=build-win2012r2x64-01/) | [![Build Status](https://jenkins.dandle.co/buildStatus/icon?job=esp-alt-sdk/VERSION=1.5.0,label=build-osx-01)](https://jenkins.dandle.co/job/esp-alt-sdk/VERSION=1.5.0,label=build-osx-01/) | [![Build Status](https://jenkins.dandle.co/buildStatus/icon?job=esp-alt-sdk/VERSION=1.5.0,label=build-ubuntu14-01)](https://jenkins.dandle.co/job/esp-alt-sdk/VERSION=1.5.0,label=build-ubuntu14-01) |

## Why?
- Cross platform
    + Windows
    + Linux
    + MacOS
- Up-to-date binary builds
- Open build process 
- Gcc 5.3.0
- Gdb 7.10.1 on all platforms
- Binutils 2.26
- Additional tools (also compiled from source)
- Small size
    + Stripped out debug symbols
    + UPX compressed

## Contents
- [GCC 5.3.0](http://ftp.gnu.org/gnu/gcc/gcc-5.3.0/gcc-5.3.0.tar.bz2) with jcmvbkbc patches
- [Espressif NONOS SDK](http://bbs.espressif.com/viewforum.php?f=46) with Espressif patches
- [lx106-hal](https://github.com/tommie/lx106-hal)
- [newlib-xtensa](https://github.com/jcmvbkbc/newlib-xtensa)
- [binutils 2.26](http://ftp.gnu.org/gnu/binutils/binutils-2.26.tar.bz2) with jcmvbkbc patches
- [gdb 7.10.1](http://ftp.gnu.org/gnu/gdb/gdb-7.10.1.tar.gz) with jcmvbkbc patches
- [esptool](https://github.com/themadinventor/esptool)
- [esptool2](https://github.com/raburton/esptool2)
- [memanalyzer](https://github.com/Sermus/ESP8266_memory_analyzer)

## Download
__Download links are still unstable, please check__ [bintray](https://bintray.com/kireevco/generic/esp-alt-sdk/view#files)

| Windows | MacOS | Linux |
| ------------- | ------------- | ------------- |
| [1.4.0](https://bintray.com/kireevco/generic/esp-alt-sdk/1.4.0/view#files) | [1.4.0](https://bintray.com/kireevco/generic/esp-alt-sdk/1.4.0/view#files) | [1.4.0](https://bintray.com/kireevco/generic/esp-alt-sdk/1.4.0/view#files) |
| [1.5.0](https://bintray.com/kireevco/generic/esp-alt-sdk/1.5.0/view#files) | [1.5.0](https://bintray.com/kireevco/generic/esp-alt-sdk/1.5.0/view#files) | [1.5.0](https://bintray.com/kireevco/generic/esp-alt-sdk/1.5.0/view#files) |
| [1.3.0-rtos](https://bintray.com/kireevco/generic/esp-alt-sdk/1.3.0-rtos/view#files) | [1.3.0-rtos](https://bintray.com/kireevco/generic/esp-alt-sdk/1.3.0-rtos/view#files) | [1.3.0-rtos](https://bintray.com/kireevco/generic/esp-alt-sdk/1.3.0-rtos/view#files) |

## Build yourself
### Windows
Install git:
```cmd
choco install git.install --params="/NoAutoCrlf" -y
```

Install ConEmu (Optional)
```cmd
choco install conemu -y
```

Clone repo, configure environment
```cmd
git clone https://github.com/kireevco/esp-alt-sdk.git
cd esp-alt-sdk
env\msys2_10.cmd
```

Start Mingw32 Shell and run:
```cmd
cd env; make
make
```

### MacOS
Clone repo, configure environment
```shell
git clone https://github.com/kireevco/esp-alt-sdk.git
cd esp-alt-sdk
./env/macos_10.sh
```

Start build
```shell
make -C env/ && make
```


### Ubuntu
Clone repo, configure environment
```shell
git clone https://github.com/kireevco/esp-alt-sdk.git
cd esp-alt-sdk
./env/ubuntu_10.sh
```

Start build
```shell
make -C env/ && make
```


-----
#### Credits:
- Max Fillipov (@jcmvbkbc) for major xtensa-toolchain heavylifting (gcc-extensa, newlib-xtensa)
- Paul Sokolovsky (@pfalcon) for esp-open-sdk and major integration work
- Fabien Poussin (@fpoussin) for xtensa-lx106-elf build script
