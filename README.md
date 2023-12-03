# backup-openwrt-ALL
Backup Openwrt

i have tested this solution and worked perfecly for me ( with router ea8300 and 2 partition...)

    1/ create backup
    tar -cvzf /tmp/overlay.tar.gz /overlay

    02/ save archive

on wincsp or other soft, access on folder /tmp and download on your desktop the file overlay.tar.gz

    4/ identify your backup

create new folder and place overlay.tar.gz inside, and create new text file and add :

    openwrt version ( for me actual 21.02.0 RC3)
    and other information if you want

FOR RESTORE BACKUP

    1/ format your system

the first edit dosen't work because if you flash sysupgrade, openwrt change partion work, please use only :
SSH : firstboot && reboot now

    3/ restore backup

    connect on winscp and place overlay.tar.gz on /tmp folder
    on SSH client
    cd /; tar -xvzf /tmp/overlay.tar.gz
    and
    reboot
