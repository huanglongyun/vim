<!--
 * @Author: hly
 * @Date: 2022-07-04 09:27:51
 * @LastEditors: hly
 * @LastEditTime: 2022-07-04 10:06:02
 * @Description:
-->
day4

目标：更有效率的处理单字符 & undo/redo

1. 删除光标所在位置的字符 x（小写）
2. 删除光标前的一个字符 X （大写）
3. 删除当前光标的字符并进入 insert 模式:s(小写)
4. 删除当前光标所在行并进入 insert 模式:S（大写）
5. 替换一个字符:r
6. 替换多个字符:R
7. undo/redo
    1. 可撤销块:进入插入模式开始,知道返回普通模式为止,在此期间输入或删除的任何内容都被当成一次修改
    2. undo : u 撤销
    3. redo : ctrl + r 恢复