1. Reboot in rescue mode
2. go to https://factory.talos.dev/
3. After generating the iso
4. Copy iso url to VPS `wget https://factory.talos.dev/image/613e1592b2da41ae5e265e8789429f22e121aab91cb4deb6bc3c0b6262961245/v1.11.2/metal-amd64.iso`
5. list disks `lsblk` and find the disk with the right volume
6. `wipefs -af /dev/sd(a|b)`
7. copy iso to disk `dd if=/root/metal-amd64.iso of=/dev/sd(a|b) bs=8M status=progress`
8. reboot vps from OVH console
9. (optional) Open KVM Console
10. 

