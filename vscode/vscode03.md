<!--
 * @Author: hly
 * @Date: 2022-07-26 08:41:12
 * @LastEditors: hly
 * @LastEditTime: 2022-07-27 08:30:48
 * @Description:+
-->
day21

目标：掌握vscode搜索

1. global search
    1. ctrl + shift + f 打开搜索
        eg：某文件选中单词（viw)，复制（ctrl+c）  ，进入资源管理器（ctrl+ ;），打开搜索（ctrl+shift+f）
    2. ctrl + up/down 切换到搜索内容
        改变一下，使用 shift+j/k 进行切换
        ```
        // keybindings.json
        // 搜索 切换到搜索内容
        {
            "key": "shift+j",
            "command": "search.focus.nextInputBox",
            "when": "inSearchEditor && inputBoxFocus || inputBoxFocus && searchViewletVisible"
        },
        {
            "key": "shift+k",
            "command": "search.action.focusSearchFromResults",
            "when": "firstMatchFocus && searchViewletVisible"
        },
        ```
    3. ctrl + shift + j 切换搜索详细信息
        由于之前改过键，直接按无效是无效的，需要在键盘快捷方式，搜 toggleQueryDetails，将默认的ctrl + shift + j 改成 shift + down ，然后就可以操作 ctrl+ shift + j 切换搜索详细信息了

2. 整个工作区进行搜索 ctrl+t

3. 当前文件下搜索 ctrl + shift + o
    : 键入冒号，按功能分类

4. 全局搜索 ctrl+shift+p

5. 搜索文件 ctrl + p

6. 文件切换
    vim
    vscode ctrl + tab
