<!--
 * @Author: hly
 * @Date: 2022-07-23 14:48:39
 * @LastEditors: hly
 * @LastEditTime: 2022-07-24 17:08:26
 * @Description:
-->
day 19

目标：操作文件

问题 键盘快捷方式用户自定义的 when 怎么设置？


1. 切换 files explorer区域 资源管理器区域
    vim : shift+ctrl+h
    vscode:默认命令 ctrl + shift + e
           改成命令 ctrl + ;
    再按一次就会回到编辑区
    键盘快捷方式搜 explorer
    ```
        // keybindings.json
        {
          "key": "ctrl+;",
          "command": "workbench.view.explorer",
          "when": "viewContainer.workbench.view.explorer.enabled"
        }
    ```

2. 切换到编辑区
    vim
    vscode:默认命令 shift + alt + 1
           改成命令 ctrl + '
    ```
        // keybindings.json
        {
          "key": "shift+'",
          "command": "workbench.action.moveEditorToFirstGroup"
        }
    ```

3. 移动光标 jk
4. 展开/折叠 l
    当是文件时，按l 打开文件

5. 创建文件
    1. 在 files explorer 中： a
    ```
        // keybindings.json
    {
      "key": "a",
      "command": "explorer.newFile",
      "when": "filesExplorerFocus && !inputFocus"
    },
    ```
    2. 在 editor
        vim : <leader> + n + f
        ```
        // 快捷键方式 搜 newfiles 复制ID
        // settings.json
        "vim.normalModeKeyBindingsNonRecursive": [
            // 新建文件
            {
                "before":["<Leader>", "n", "f"],
                "commands":["explorer.newFile"]
            }
        ]
        ```
    3. vscode : ctrl + n
    4. 使用插件 file utils

6. 创建文件夹
    1. 在files explorer 中 :A
        ```
        // keybindings.json
    {
      "key": "shift+a",
      "command": "explorer.newFolder",
      "when": "filesExplorerFocus && !inputFocus"
    },
    ```

    2. 在 editor
        vim : <Leader> + n + d
                ```
        // 快捷键方式 搜 newfolder 复制ID
        // settings.json
        "vim.normalModeKeyBindingsNonRecursive": [
            // 新建文件
            {
                "before":["<Leader>", "n", "f"],
                "commands":["explorer.newFile"]
            }
        ]
        ```
    3. 使用插件 file utils