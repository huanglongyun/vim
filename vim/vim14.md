<!--
 * @Author: hly
 * @Date: 2022-07-17 21:21:56
 * @LastEditors: hly
 * @LastEditTime: 2022-07-18 09:04:01
 * @Description:
-->
<!--
 * @Author: hly
 * @Date: 2022-07-17 21:21:56
 * @LastEditors: hly
 * @LastEditTime: 2022-07-17 21:25:55
 * @Description:
-->
day14

目标：掌握悬浮显示 & 大小写 & 注释

内容少，用处大，解决了常量输入问题，注释也很方便

1. 悬浮显示 gh (hover, 鼠标放到单词上出现的悬浮内容)
    取消显示用 esc 或 ctrl [

2. 大小写
    1. normal模式
        1. gu 变小写
        2. gU 表大写
            eg: 先用小写写好单词，进入normal模式，gUiw
    2. 可视化模式
        1. u
        2. U
    3. 大小写互换 ~

3. 注释
    1. gc 单行注释 //
        eg: gcl 注释当前行
            gcj 注释当前行和下一行
    2. gC 多行注释 /** */
        eg: gCiw 注释一个单词 import {/* name*/} from 'xxx'

    tips : normal 和 可视化通用

ve 选中一个单词，光标在词首

    NAME_KEY