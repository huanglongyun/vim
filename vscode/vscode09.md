<!--
 * @Author: hly
 * @Date: 2022-08-03 09:00:12
 * @LastEditors: hly
 * @LastEditTime: 2022-08-04 09:12:06
 * @Description:
-->
day28

目标：VSpaceCode（whichkey）
    VSpaceCode：vim用户
    whichkey：普通用户
    两者区别不大

    各有各的好处吧，能形成肌肉记忆，也就不怎么需要这个面板提示了

1. 安装 https://marketplace.visualstudio.com/items?itemName=VSpaceCode.vspacecode

2. 初始化
    1. settings https://github.com/VSpaceCode/VSpaceCode/blob/master/src/configuration/settings.jsonc
        配置开启命令，默认是 空格键，但是空格之前已经使用，现在配成 空格 + ;
        ```
        // settings.json
         "vim.normalModeKeyBindingsNonRecursive": [
            {
                "before": ["<space>",";"],
                "commands": ["vspacecode.space"]
            }
        ]
        ```

    2. keybindings https://github.com/VSpaceCode/VSpaceCode/blob/master/src/configuration/keybindings.jsonc
        上面的配置只作用于编辑区，要作用在资源管理器，还需设置
        配置 space 开启
        ```
        // keybindings.json
        // Trigger vspacecode in empty editor group
        {
            "key": "space",
            "command": "vspacecode.space",
            "when": "activeEditorGroupEmpty && focusedView == '' && !whichkeyActive && !inputFocus"
        },
        // Trigger vspacecode when sidebar is in focus
        {
            "key": "space",
            "command": "vspacecode.space",
            "when": "sideBarFocus && !inputFocus && !whichkeyActive"
        },
        ```
3. 在原有基础上进行修改
    1. 修改/增加

4. ⾃定义⾃⼰的 "vspacecode.bindings": []

5. 不喜欢弹窗的话 可以⾃⼰配置 vim
    github.com/VSpaceCode/VSpaceCode/tree/vscode-vim
