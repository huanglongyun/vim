<!--
 * @Author: hly
 * @Date: 2022-07-09 21:21:48
 * @LastEditors: hly
 * @LastEditTime: 2022-07-09 22:14:36
 * @Description:
-->
day8

目标：掌握搜素

1. 单行
    1. f 正向移动到下一个{char}所在之处
    2. F 反向移动到上一个{char}所在之处
    3. t 正向移动到下一个{char}所在之处的前一个字符上
    4. t 反向移动到上一个{char}所在之处的前一个字符上
    5. ; 重复上一次的字符查找命令
    6. , 反转方向重复上一次的字符查找命令
    7. 使用技巧
        1. 移动的时候用 f
        2. 结合 c / d  使用 t
            eg：d t 字符 删除光标到某个字符之前的之间的内容
                v f 字符 选择光标到某个字符之间的内容

2. 全局
    1. / 向后查
        按下 / 后会在做最底部出现一个框可以输入要查找的内容，按 回车 后进行查找，按 n 重复查找命令, 按 N 反向重复查找命令
    2. ? 向前查
    3. n / N
    4. / 上下放下键 查看搜素历史
    5. 技巧 写单词的前几个字母就可以
    6. # 向上查 严格查找 会区分大小写
    7. * 向下查
    eg: d / 内容 回车 删除光标到查找内容前之间的内容


    很多技巧没有老师教，自己确实想不到

```

hfkskd hfls dkskflh flsd flshfl flsdf lfslf
dhfs jskdffl 你好 kfksdfj 我在找你fjd hffhs
dfksdf ddslf
jack
jack
jack
job
job
jack
job
jack
jack

hdhfks djsdfj

function getName(value){
    let a = 99
}

```