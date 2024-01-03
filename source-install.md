## building and installing from source for:

 - [ubuntu](#For-ubuntu)

 

### For ubuntu:
```bash
# Initialize build system (only required once per repo)
meson build -D ubuntu=true
cd build

# Build and install
sudo ninja install

# Install the ubuntu-bgrt plymouth-theme with priority
sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/ubuntu-bgrt/ubuntu-bgrt.plymouth 200

# Update-initramfs
sudo update-initramfs -u
```
