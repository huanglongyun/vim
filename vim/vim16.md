<!--
 * @Author: hly
 * @Date: 2022-07-19 09:17:44
 * @LastEditors: hly
 * @LastEditTime: 2022-07-19 10:24:13
 * @Description:
-->
day16

目标：如何删除一个函数

1. % 匹配括号 () [] {} 自动匹配另一侧的括号
    eg:v% 在可视化模式下，光标在一侧括号上，按 v% 即可快速选中包含括号的内容

2. 插件 vim-indent-object 基于缩进选择范围
    vii 选中函数体内
    vai 选中函数体内 加上函数名，但不包括函数最后的}. 通过改vscode映射 可实现 VaI 功能
    vaI 选中函数体

3. 删除方式
    1. dap \ dip 基于段落 text-object. 只能按段落删，函数内有空格的话就会断开，不能删全
    2. daI 基于vim-indent-object 光标得在函数体内才行，
        映射改键 在vscode中，将小写的i 改成 I。ai => aI ai连着一起打
        ```
            "vim.visualModeKeyBindings": [
                {
                    "before":["a","i"],
                    "after":["a","I"]
                }
            ],
            "vim.operatorPendingModeKeyBindings": [
                {
                    "before":["a","i"],
                    "after":["a","I"]
                }
            ],
        ```
    3. V$%d V 选中当前行，$ 到行尾, % 匹配括号， d 删除
        1. 优化 =>使用配置: 空格df <leader> 空格， d 删除，f 函数
        ```
            "vim.normalModeKeyBindings": [
                {
                    "before":["<leader>","d","f"],
                    "after":["V","$","%","d"]
                }
            ],
        ```
        2. 参数多个的话 就使用两次 V$%$%
        3. 光标得在函数这一行



```
function clog(value){
    return console.log(value)
}

function getName(value){
    const name = value
    if(!name){
        return 99
    }

    return name
}
```