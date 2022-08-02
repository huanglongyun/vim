<!--
 * @Author: hly
 * @Date: 2022-07-22 09:43:52
 * @LastEditors: hly
 * @LastEditTime: 2022-07-22 16:59:23
 * @Description:
-->
day18

目标：vim调用vscode命令

学会vim 调用 vscode命令的方法
用vim命令替换vscode命令
在settings.json中改键设置
在keyboard 快捷方式中，查找到vdcode的命令id

1. commands 字段

2. 使用
    格式化文档
        vscode 中的命令 shift + alt + f
        vim 中的命令 <Leader> + f + d
        ```
            "vim.normalModeKeyBindings": [
                {
                    "before":["<leader>","f","d"],
                    "commands":["editor.action.formatDocument"]
                }
            ],
        ```
    重命名
        vscode 中的命令 f2
        vim 中的命令 <Leader> + r + n
        ```
            "vim.normalModeKeyBindings": [
                {
                    "before":["<leader>","r","n"],
                    "commands":["editor.action.rename"]
                }
            ],
        ```
    折叠代码
        vscode 中的命令 ctrl + shift + [
        vim 中的命令 <Leader> + [
        ```
            "vim.normalModeKeyBindings": [
                {
                    "before":["<leader>","["],
                    "commands":[{
                    "command": "editor.fold"
                    },{
                    "command":"vim.remap",
                    "args":{
                        "after":["$","%"]
                    }
                    }]
                }
            ],
        ```