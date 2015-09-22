# Troubleshooting


### Issues expanding the root filesystem via raspi-config
This can occur for large sdhc cards, typically `32gb` or larger.

* Try running the filesystem expansion directly:
  * View disk partition info: `sudo fdisk -cu /dev/mmcblk0`
  * Note the current partition, typically `mmcblk0p2`
  * Resize directly: `sudo resize2fs /dev/mmcblk0p2`
  * `sudo raspi-config`, then `Expand root filesystem`
  * `sudo reboot`
  
