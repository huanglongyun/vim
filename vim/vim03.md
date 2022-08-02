<!--
 * @Author: hly
 * @Date: 2022-07-03 10:20:33
 * @LastEditors: hly
 * @LastEditTime: 2022-07-29 18:00:22
 * @Description:
-->
day3

目标：掌握vim语法

语法：操作 + 动词（范围 k j h l 0 g_）
    dh d 操作，h 范围，删除光标左侧的一个字符
    dl 删除当前光标选中的字符


操作
    删除 d
    删除并进入insert模式 c
    复制 y

基于单词/字串的移动
    e 移动到单词的结尾 符号会被当成单词
    w 移动到单词的开头
    b 移动到上一个单词的开头
    ge 移动到上一个单词的结尾
    字串用大写
组合
    cw 删除当前单词(光标要在单词词首)
    ea 在当前单词结尾处添加


 kdksd jdkfjkldf
you're good
function getName(){
    return 1
}