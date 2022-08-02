<!--
 * @Author: hly
 * @Date: 2022-07-14 08:46:34
 * @LastEditors: hly
 * @LastEditTime: 2022-07-14 09:49:38
 * @Description:
-->
day12

目标:处理包裹字符的符号

在敲cs ys ds 时 两个字母的间隔时间要小，间隔太长的话 不起效，找了一圈没发现不起效的原因，最后发现是手速不行。
处理包裹字符的符号这个知识，又使开发效率提高了一些

插件 vim-surround
    在normal模式下
        修改：Change existing surround to desired
            => c s <existing> <desired>
            => cs 已存在的符号 期望符号
            eg: cs ' " => 将 'name' 中的 '' 改成 ""
        增加：Add desired surround around text defined by
            => y s <motion> <desired>
            => ys 范围 期望符号
            eg:ys iw { => 给 add 加上 {}
        删除：Delete existing surround
            => d s <existing>
            => ds 要删除的符号
            eg:ds " => 删除 "name" 的 ""

    在visual模式下
        给选中的内容添加符号 ：Surround when in visual modes (surrounds full selection)
        => S <desired>
        => S 期望符号

import add from './demo.js'
const a = 'zhangsan'

sNativcseTag