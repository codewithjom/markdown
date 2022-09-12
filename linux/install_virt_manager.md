# :point_right: Install Virt Manager

## Table of Contents
- [Installation](#installation)
- [Enable lib-virt in Daemon](#daemon)
- [Create a Bridge Interface](#bridge)
- [Convert From Vbox to Qemu](#convert)

### Installation <a id='installation'></a>

``` sh
sudo pacman -S virt-manager qemu qemu-arch-extra ovmf vde2 ebtables dnsmasq bridge-utils openbsd-netcat
```

### Enable lib-virt in Daemon <a id='daemon'></a>

``` sh
sudo systemctl enable libvirtd.service
sudo systemctl start libvirtd.service
```

### Create a Bridge Interface <a id='bridge'></a>

``` sh
sudo vim .br10.xml
```

Paste this to your xml file.

``` xml
<network>
  <name>br10</name>
  <forward mode='nat'>
    <nat>
      <port start='1024' end='65535'/>
    </nat>
  </forward>
  <bridge name='br10' stp='on' delay='0'/>
  <ip address='192.168.30.1' netmask='255.255.255.0'>
    <dhcp>
      <range start='192.168.30.50' end='192.168.30.200'/>
    </dhcp>
  </ip>
</network>
```

Run this on your terminal.

``` sh
sudo virsh net-define .br10.xml
sudo virsh net-start br10
sudo virsh net-autostart br10
```

### Convert From Vbox to Qemu <a id='convert'></a>

Run this command if you want to run your .vdi to virt manager. Let's convert the .vdi to .qcow2 and place it to `/var/lib/libvirt/images/archlinux.qcow2`.

``` sh
sudo qemu-img convert -f vdi -O qcow2 archlinux.vdi /var/lib/libvirt/images/archlinux.qcow2
```
