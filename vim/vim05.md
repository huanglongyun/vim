<!--
 * @Author: hly
 * @Date: 2022-07-06 10:50:14
 * @LastEditors: hly
 * @LastEditTime: 2022-07-06 15:30:17
 * @Description:
-->
day5

目标：掌握可视化模式 visual block

可视化模式
    字符：v
    行：V
    块：C-V
    以上三种模式可任意切换

退出
    esc
    c-[
    V 用上面另种，v V容易忘记忘记步骤
    v

导航
    配合动作范围
    o 切换可视区的光标位置，光标在选中内容的首行和尾行跳转
    gv 回到上一次选择的选择区域

语法
    选中+ 操作

技巧
    1. 跨多行编辑，给多行的选中区域加内容，配合 A（选中区域后加） 或 I（在选中区域前加）
    2. 赋值粘贴：利用系统的剪切板
        改键：在win下，用到visual block，按ctrl + v的话，又会变成粘贴，进不去visual block模式，可以把handleKeys指定的C-v配成true就可以了
        "vim.handleKeys": {
            "<C-v>": true,
        }
    3. 尽可能的少用可视化模式:会增加操作步骤


    ve 光标在词首，选中一个单词
    V 选中当前行
    v + kjhl 可进行选中范围控制

练习
```
const a - c = 1
const b - c = 2
const c - c = 3
```

体会
    1. 看就会，用就废，看视频时感觉自己会了，用的时候就是想不出来，得来回看好多次，脑子不够用
    2. 练的少，效果也就不怎么好