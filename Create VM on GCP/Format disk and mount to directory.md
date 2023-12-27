1.  Check block disk name [lsblk](https://www.geeksforgeeks.org/lsblk-command-in-linux-with-examples/)
    -  ```lsblk```<br />
      <img src="images/x1. lsblk.png" height="50" />       

2.  Check disk name to [fdisk](https://www.geeksforgeeks.org/fdisk-command-in-linux-with-examples/)
    -  ```fdisk -l```<br />
      <img src="images/x1. lsblk.png" height="50" />

3.  Format Disk
    -  ```
       sudo fdisk /dev/sdb
       n
       <enter for default>
       <enter for default>
       <enter for default>
       <enter for default>
       t
       8e
       p
       w
       ```
      <img src="images/x3. Format disk 1.png" height="50" /><br />
      <img src="images/x4. Disk has been formatted.png" height="50" />

4.  Create New Physical Volume ([pvcreate](https://www.thegeekdiary.com/pvcreate-command-examples-in-linux/)), Volume Group ([vgcreate](https://www.thegeekdiary.com/vgcreate-command-examples-in-linux/)), and Format Disk to XFS ([lvcreate](https://www.thegeekdiary.com/lvcreate-command-examples-in-linux/))
    -  ```
       sudo pvcreate /dev/sdb1
       sudo vgcreate data /dev/sdb1
       sudo lvcreate -n data -l 100%FREE data /dev/sdb1
       sudo mkfs.xfs /dev/data/data
       ```
      <img src="images/x5. Create physical, volume group, logical volume, and format disk to XFS.png" height="50" />

5.  Create new Directory and Mounting Logical Volume to spesific directory
    -  ```
       sudo mkdir /data
       sudo mount /dev/data/data /data
       ```
      <img src="images/x6. Mounting Logical Volume to Directory.png" height="50" />

6.  Save Mounting Logical Volume [fstab](https://en.wikipedia.org/wiki/Fstab)
    -  ```
       sudo vim /etc/fstab
       ```
    -  Add this line to /etc/fstab
       ```
       /dev/data/data			/data				xfs			default					0 0
       ```
      <img src="images/x7. Edit the FSTAB for permanent mounting logical volume to directory.png" height="50" />

