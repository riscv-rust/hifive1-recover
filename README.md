# `hifive1-recover`

> Bootloader recovery scripts for HiFive1 boards

## Dependencies

To restore bootloader on your board you need programmer software. This is basically the same software that was mentioned in the `riscv-rust-quickstart` repo.

For HiFive1 Rev B: [Segger JLink software & documentation pack for Linux](https://www.segger.com/downloads/jlink/)

For HiFive1: [OpenOCD from SiFive](https://static.dev.sifive.com/dev-tools/riscv-openocd-0.10.0-2019.02.0-x86_64-linux-ubuntu14.tar.gz). You can also use a fresh upstream OpenOCD build (available as `openocd-git` in ArchLinux, for example).

## Recovering the bootloader

Clone the repository:

``` console
git clone https://github.com/riscv-rust/hifive1-recover
cd hifive1-recover
```

Alternatively, you can download it as a [zip file](https://github.com/riscv-rust/hifive1-recover/archive/master.zip) and unpack:
``` console
wget https://github.com/riscv-rust/hifive1-recover/archive/master.zip
unzip master.zip
cd hifive1-recover-master
```

### HiFive1 Rev B

Make sure `JLinkExe` is in path, otherwise add it:
``` console
PATH=$PATH:/path/to/JLink  # /tmp/JLink_Linux_V683b_x86_64, for example
```

Connect the board and run the `recover` script:
``` console
cd hifive1-revb
./recover
```

### HiFive1

Make sure `openocd` is in path, otherwise add it:
``` console
PATH=$PATH:/path/to/riscv-openocd-0.10.0-2019.02.0-x86_64-linux-ubuntu14/bin
```

Connect the board and run the `recover` script:
``` console
cd hifive1
./recover
```

## Troubleshooting

If something doesn't work for you, feel free to [open an issue](https://github.com/riscv-rust/hifive1-recover/issues/new).
