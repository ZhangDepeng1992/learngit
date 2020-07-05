#Linux学习笔记
##linux 弹出U盘: 目标忙 解决方案
###1. 查看挂载点
`df -h`
###2. 使用`umount`弹出U盘报错
使用`top c`，发现没有使用U盘的程序。

使用`fuser -mv /mnt/p2`查看U盘的uid，杀死这个进程
###3. 查看U盘的uid
使用kill杀死
`kill -9 uid`
###4. 使用`umount`弹出U盘
`umount /mnt/p2`