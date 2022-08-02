<!--
 * @Author: hly
 * @Date: 2022-07-07 08:46:20
 * @LastEditors: hly
 * @LastEditTime: 2022-07-07 10:56:17
 * @Description:
-->
day6

目标：掌握文本对象

认识文本对象
    文本是结构化的，可以快速选择
    范围

语法
    operator + （内部/外部）+ 文本对象
        可视化模式 + （内部/外部）+ 文本对象  => v +（i/a) + 文本对象

内部 i

外部 a

文本对象
    w :一个单词
    b ( ) : 一对()
    [ ] : 一对[]
    B { } : 一对{}
    < > : 一对<>
    t : XML标签
    ' : 一对 ''
    " : 一对 ""
    ` : 一对 ``
    s : 一个句子
    p : 一个段落
    vim-textobj-arguments vim插件 匹配arguments 如 处理参数 (name, age) 光标在 g
        ia 不包含分隔符 => age
        aa 包含分隔符  => , age
        技巧
            删除一个参数 daa => 删除age，连同前面的 ， 也要一起删除
            修改一个参数 cia
    vim-textobj-entire 匹配所有文本对象
        ae 删除当前文本所有内容
        ie 删除当前文本所有内容, 打不包含前面后后面的空格

v i w 选中光标所在位置的单词
v e   选中光标所在位置到单词结尾之间的内容，
c i w 删除光标所在单词
v i ( 选中括号内的内容
v a ( 选中包含括号在内的内容
d i ( 删除括号内的内容

又增加很多炫酷的操作，感觉很方便，就是记不住。主要还是练的少，速度慢，
```
function getName(data){
    const a = '997'
    cosnt b = "hfkdfj"
    cosnt c = `hfsdkfjsd`
    return data
}

<div>你好呀 我不好</div>
fskjf jfsdkfj jfdskf
fhsdfk fkdhfs jfdj.
fsk hfksdh dhfks?
fjejf fkdj jfdj!
```