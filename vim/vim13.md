<!--
 * @Author: hly
 * @Date: 2022-07-16 09:20:03
 * @LastEditors: hly
 * @LastEditTime: 2022-07-17 21:25:53
 * @Description:
-->
day13
目标：替换字符

1. 替换命令 :substitute
    1. 公式 :[range]s[ubstitute]/{pattern}/{string}/[flags]
        [] 中括号内的内容可以省略
        s[ubstitute] 可以写全名 substitute,也可以用s代替，
        要按回车才生效
        eg：将 test 替换成 haha => :s/test/haha 回车
    2. range :范围
        1. % 全文 全文替换 *
            每一行的第一个
            eg: :%s/旧内容/新内容 回车
        2. number:number 基于行的选择，可从第几行到第几行，用 , 隔开
            eg: :2,4s/旧内容/新内容 回车
        3. $ 到尾部 和number类似到行尾 2,$
            eg: :2,$s/旧内容/新内容 回车
    3. pattern 模式 正则替换
        eg: :%s/h\d/test 回车 => 将 h1 和 h2 替换成 test
            :%s/h[12]/test 回车 => 将 h1 和 h2 替换成 test

    4. flag
        1. g 全局替换，包含全部的，不光是第一个
            eg: :%s/旧内容/新内容/g 回车
        2. c 讯问式替换
            y 当前项替换
            n 跳过当前项
            a 全部替换
            q 退出
            l 只替换第一个
    5. 可视化模式下 ： 全局替换

2. 多选操作
    gb 多选，区分大小写，可用于多光标选中



haha
haha
test
test
test
Test
test test

ee
v1 v1