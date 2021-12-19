# Steps-to-Start-with-the-Spike-Emulator
mkdir RISC-V
cd RISC-V
git clone $ git clone https://github.com/riscv/riscv-gnu-toolchain

mkdir RISC-V
mkdir RISCV
git clone --recursive https://github.com/riscv/riscv-gnu-toolchain
cd riscv-gnu-toolchain
$ git log
$ sudo apt-get install autoconf automake autotools-dev curl python3 libmpc-dev libmpfr-dev libgmp-dev gawk build-essential bison flex texinfo gperf libtool patchutils bc zlib1g-dev libexpat-dev

./configure --prefix=/opt/riscv
make
./configure --prefix=/opt/riscv --with-arch=rv32gc --with-abi=ilp32d
.make linux

./configure --prefix=$RISCV --disable-linux --with-arch=rv64ima 
.make linux


riscv pk
$ mkdir build
$ cd build
$ ../configure --prefix=$RISCV --host=riscv64-unknown-elf
$ sudo make
in header file machine/mtrap.h line 51 change char with uintptr_t
$ sudo make install 

spike simulator
$ apt-get install device-tree-compiler
$ mkdir build
$ cd build
$ ../configure --prefix=$RISCV
$ make
$ [sudo] make install

