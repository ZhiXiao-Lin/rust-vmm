# Rust VMM

## Quick start

### Prerequisites

Make sure you have a compiled linux kernel with a initramfs configured before you start.

If you don't have one, follow these steps :

- Make a basic rootfs :

```bash
./rootfs/mkrootfs.sh
```

- Build a linux kernel :

```bash
./kernel/mkkernel.sh
```

Press enter when `Built-in initramfs compression mode` is asked.

### Build

```bash
cargo build --release
```

### Run

```bash
./target/release/rust-vmm --kernel ./linux-cloud-hypervisor/arch/x86/boot/compressed/vmlinux.bin
```

You should see this in your console :

```bash
/ #
```

To see all the available arguments :

```bash
./target/release/rust-vmm --help
```
