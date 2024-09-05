# This process will create the clone of SD card that can run on other edge device like raspberry pi.

## Step 1: Check the card mopunt
```
lablk or sudo fdisk -l
```

## Step 2: Command top clone the card
```
sudo dd if=/dev/sdx of=/path/to/backup.iso bs=4M status=progress
```
## Step3: Verify 
```
sudo dd if = /dev/sdx bs = 4M | md5sum
md5sum /path/to/backup.iso
```
if both checksum are qual then card is clone perfect
