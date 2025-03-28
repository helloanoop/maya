# maya

An operating system. Everyone needs a hobby. This is mine.

### Dependencies
```bash
# Install qemu
brew install qemu

# Install nasm
brew install nasm
```

### Development
```bash
# Build the bootloader
nasm -f bin boot.asm -o boot.bin

# Disassemble the bootloader
ndiasm boot.bin
```

### Run the bootloader
```bash
# Run the bootloader
qemu-system-x86_64 -drive file=boot.bin,format=raw
```