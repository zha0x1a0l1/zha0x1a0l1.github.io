---
title: 删除Ubuntu系统
date: '2009-04-16 00:00:00'
slug: shan-chu-Ubuntu-xi-tong
categories:
- 科技
tags:
- 科技
- Linux
- 软件
---
118、Uninstall Ubuntu(删除Ubuntu系统)
When used on a dual-boot computer, the following steps will restore the Windows boot loader and then remove the Ubuntu partitions。
（这是针对于Windows与Ubuntu双启动系统的操作）
1. Insert your Windows installation CD and boot from it. When the initial installation choices menu appears, hit r to get to the Recovery Console. Select your Windows partition when prompted, and enter the Administrator password when prompted (if you didn’t set an administrator password, just hit Enter ).
（插入Windows系统安装盘启动电脑，在安装选择菜单出现的时候，按R键进入系统修复模式，然后选择到你的Windows分区，回车）
2. Type the following commands, the last of which will reboot your computer:
（输入下列命令，输入完后电脑重新启动）
C:\> fixmbr
C:\> fixboot
C:\> bootcfg /rebuild
C:\> exit
3. You should now be able to boot into Windows when the computer is rebooted, but to delete the Ubuntu partitions and enlarge the Windows partition you’ll need to boot from your Ubuntu CD and use Gparted. Select the Try Ubuntu option from the Ubuntu installer boot menu and once Ubuntu is up and running, click System ! Administration ! Partition Editor.
（删除Ubuntu分区。用Ubuntu安装盘启动系统，启动后选择“试用Ubuntu而不改变计算机”，进入系统后，选择“系统-系统管理-分区编辑器”）
4. Look for your Ubuntu swap partition in the list—it will probably be identified as linux-swap. Right-click it and then select Swapoff from the menu that appears.
（在列表中找到交换分区，右击选择删除）
5. Select the main Ubuntu partition (it will be identified as ext3 in the list), right-click and select Delete. Repeat with the linux-swap partition. Note that the two partitions might be in an extended partition. You may need to select this too and then select Delete.
（删除列表中的所有Ubuntu分区）
6. Right-click the NTFS (Windows) partition and select Resize/Move.Then, in the dialog that appears, click and drag the right-edge of the graphical representation of the partition until it fills the disk. Click the Resize/Move button. Then click the Apply button in the main Gparted window. Note that if you see an error during NTFS resizing, it’s likely you didn’t shutdown Windows properly the lastBtime you used it. Reboot into Windows and run a chkdsk. Then repeat this step.
7. There’s one last thing to take care of—getting rid of the Windows boot menu we introduced when restoring theWindows boot loader. Using My Computer, browse to the root of C:\ and right-click boot.ini (ensure you have chosen to show invisible files in Tools ! Options). Click Properties and remove the check from the Read Only box. Then open  :\boot.ini in Notepad, and change the timeout=30 line to read timeout=0. Save the file and reboot to test.

---


