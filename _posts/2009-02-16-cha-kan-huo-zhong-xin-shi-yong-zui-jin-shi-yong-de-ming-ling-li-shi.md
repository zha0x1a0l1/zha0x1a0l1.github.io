---
title: 察看或重新使用最近使用的命令历史
date: '2009-02-16 00:00:00'
slug: cha-kan-huo-zhong-xin-shi-yong-zui-jin-shi-yong-de-ming-ling-li-shi
categories:
- 杂项
tags: []
---
2、See (and reuse) the most recently typed commands（察看或重新使用最近使用的命令历史）
history –这个命令是打开home下的 .bash_history，这里存放了最近使用的1000条命令
history | less pipe the output into a text reader (以文本形式显示)
To reuse one of your commands, at the command-prompt type an exclamation mark and then the number alongside the entry in the history list 。
(重新使用以前用过的命令，只需在命令的历史中所标记的数字前加上“！“号即可。)
For example, on my system, I noted when viewing the history list that the command cp /etc/fstab ~/Desktop was command 591. To use it again, I typed !591 at the command-prompt. If you ever need to simply repeat a command you’ve just used, type two exclamation marks—!!.
(例如：在察看我敲击过的历史中，注意到曾经使用过cp /etc/fstab ~/Desktop，并在历史中标记为591，再想使用这条命令，只需敲!591即可。使用刚刚使用过的命令，就敲!!即可。)
To actively rifle through your command history, hit Ctrl + r and then start typing the command you’re interested in. The prompt will “autocomplete” as you type. To use the command, hit Enter .
(按Ctrl+R，开启终端自动输入功能（自动显示的内容为你曾经使用过的历史），当出现你要输入的内容是，按回车键确认。)
To edit it before using it, hit Esc and then make your changes. Hitting the up and down cursor keys will also let you move through the most recently ommands typed. Just hit Enter when you find the one you want to reuse.
(在按回车键之前，可以按Esc键，然后再用光标对自动显示的内容进行更改，然后按回车键执行操作。)

---


