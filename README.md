# vim--基本命令
vim有三种模式：normal模式、insert模式、命令模式

历史命令
以：和/开头的命令都有历史记录 可以通过上下箭头选择历史命令
- i  -->insert插入模式 按esc回到normal模式
- x -->删除光标所在的一个字符
- :wq -->存盘+退出(:w后面可以跟文件名)
- :q -->不保存退出
- dd 删除当前行并剪切复制，相当于mac下command+x

- p 粘贴 相当于Mac下command+v



hjkl移动光标（推荐使用）,也可以使用光标键←↓↑→   注：h就像右箭头一一对应。

:help (mommand) -->显示帮助的命令，也可以使用:help不跟命令



会使用以上命令就可以编辑vim了，建议可以下意识的操作这些命令，再继续进行下一阶段。




在一般的编辑器下，当你需要copy一段文字的时候，你需要使用 Command 键，比如：Command+c。也就是说，Command 键就好像功能键一样，当你按下了功能键Command后，C就不在是C了，而且就是一个命令或是一个快键键了，再在VIM的Normal模式下，所有的键就是功能键。



1.各种插入命令

i 在当前光标位置前插入
I 在当前行首插入
a 在当前位置后插入
A在当前尾插入
o 在当前行后插入一个新行
O 在当前行前插入一个新行
cw 替换从光标所在位置后到一个单词结尾的字符
2.简单的移动光标 到本行第一个不是blank字符的位置（所谓blank字符就是空格，tab，换行，回车等）
h,j,k,l  左 下 上 右，可以结合数字使用，eg: 10j
0 数字零到行头
$ 移动到本行行尾
^ 到本行第一个不是blank字符的位置（所谓blank字符就是空格，tab,换行，回车等）
g_到本行最后一个不是blank字符的位置
gg 移动到文件头
G(shift+g)移动到文件尾
command+e 向下滚动一行
command+d 向下滚动半屏
command+f 向下滚动一屏
command+y 向上滚动一行
command+u 向上滚动半屏
command+b 向上滚动一屏
/list 搜索list字符串（如果搜索到多个匹配，可以按n键到下一个）
3.拷贝/黏贴

p 粘贴
yy 拷贝当前行，相当于ddP
4.撤销和重做
u 撤销
U 反撤销

启动命令
vim 启动
vim filename 打开vim并创建名为filename的文件
文件命令
vim file 打开某一个文件
vim file1 file2 file3 在窗口中打开多个文件
:open file 在新窗口中打开一个新文件
:split file 切换到下一个文件
:bn (:n)切换到下一个文件
:bp 切换到上一个文件
:e <path/to/file>→ 打开一个文件
:w → 存盘
: saveas <path/to/file>→ 另存为 <path/to/file> 
: x ,  ZZ或 :wq → 保存并退出 (:x 表示仅在需要时保存，ZZ不需要输入冒号并回车)
:q!→ 退出不保存 :qa!强行退出所有的正在编辑的文件，就算别的文件有更改。
