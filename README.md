# CUSTOM_debian_ISO_maker.sh
A script that builds your custom debian iso from your preseed and more 

```
rm -R /home/$USER/debian-iso-builder/iso; 
rm -R /home/$USER/debian-iso-builder/keys; 
rm -R /home/$USER/debian-iso-builder/mnt; 
rm /home/$USER/debian-iso-builder/preseed.cfg; 
rm /home/$USER/debian-iso-builder/debian-base.iso; 
rm /home/$USER/debian-iso-builder/custom-deb.iso; 
#cp /home/$USER/debian-iso-builder-VERSION_2.0.0/CUSTtrixieISOmaker4.sh /home/$USER/debian-iso-builder/CUSTtrixieISOmaker.sh; 
cd .. && chmod -R 777 debian-iso-builder;
bash /home/$USER/debian-iso-builder/CUSTtrixieISOmaker.sh && sudo dd if='/home/$USER/debian-iso-builder/custom-deb.iso' of=/dev/sdX bs=4M status=progress oflag=sync #sdX! check your drive with : lsblk
```
