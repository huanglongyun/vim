<!--
 * @Author: hly
 * @Date: 2022-07-18 09:02:07
 * @LastEditors: hly
 * @LastEditTime: 2022-07-25 14:41:25
 * @Description:
-->
day15

目标: 掌握窗口管理

1. vim新建窗口
    左右切分 Ctrl-w v
    上下切分 Ctrl-w s

2. vim窗口切换
    Ctrl-w kjhl 上下左右选择窗口，可进入vscode资源管理器 但是就不用再回到右侧窗口，因已脱离vim环境
    Ctrl-w w 互换

3. vim关闭窗口 Ctrl-w c 关闭当前光标所在的文件

4. vim只保留当前窗口，关闭其他所有的窗口 Ctrl-w o

5. 利用vscode 的自定义快捷键
    1. 新建窗口
        左右 Ctrl \
        上下 Ctrl Alt \
            设置快捷键，vscode中无向上拆分编辑器，在命令中搜索 split editor up 进入设置，进行自定义设置
    2. 关闭窗口
        ctrl w 关闭当前窗口
        Ctrl k w 关闭其他窗口  不起效
    3. 窗口切换
        shift 方向键
        我这里需要按 ctrl + shift + jkhl 进行窗口切换
        ```
            // keybindings.json

            // window move left
            {
                "key": "shift+left",
                "command":"vim.remap",
                "when": "vim.mode == 'Normal'",
                "args":{
                    "after":["C-w","h"]
                }
            },
        ```