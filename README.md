# Домашнее задание к занятию "3.5. Файловые системы"
1. Разряженные файлы - файлы в котором последовательности нулевых байт заменены на информацию о количестве этих байт. Считается одним из способов сжатия информации.
2. Нет. Жёсткие ссылки ссылаются на определенный inode. Таких жёстких ссылок может быть несколько, но все они ссылаются на один реальный файл у которого есть владелец и определенные права доступа, следственно все жёсткие ссылки на этот файл будут иметь тогоже владельца и права доступа.
3. Виртуальная машина переконфигурирована:  
   ![fdisk](./pictures/fdisk.PNG)
4. Диск /dev/sdb разбит:  
   ![fdisk sdb](./pictures/fdisk%20sdb.PNG)
5. Таблица разделов перенесена на /dev/sdc:  
   ![sfdisk](./pictures/sfdisk.PNG)
6. RAID 1 собран на /dev/sdb1 и /dev/sdc1:  
   ![mdadm RAID 1](./pictures/mdadm%20RAID%201.PNG)
7. RAID 0 собран на /dev/sdb2 и /dev/sdc2:  
   ![mdadm RAID 0](./pictures/mdadm%20RAID%200.PNG)
8. pv на /dev/md0 и /dev/md1 созданы:  
   ![pvcreate](./pictures/pvcreate.PNG)
9. Volume group создана:  
   ![vgcreate](./pictures/vgcreate.PNG)
10. LV создан:  
    ![lvcreate](./pictures/lvcreate.PNG)
11. Файловая система создана:  
    ![mkfs.ext4](./pictures/mkfs.ext4.PNG)
12. Раздел смонтирован:  
    ![mount](./pictures/mount.PNG)
13. Тестовый файл помещен в директорию ```/tmp/new/```:  
    ![wget](./pictures/wget.PNG)
14. Вывод команды ```lsblk```:  
    ![lsblk](./pictures/lsblk.PNG)
15. Целостность файла протестирована:  
    ![gzip](./pictures/gzip.PNG)
16. Содержимое PV перемещено с RAID0 на RAID1:  
    ![pvmove](./pictures/pvmove.PNG)
17. Выполнен ```mdadm --fail``` на RAID1:  
    ![mdadm fail](./pictures/mdadm%20fail.PNG)
18. Вывод dmesg, подтверждающий что RAID1 работает в деградированном состоянии:  
    ![dmesg](./pictures/dmesg.PNG)
19. Файл по прежнему доступен:  
    ![gzip 2](./pictures/gzip%202.PNG)
20. Хост уничтожен.