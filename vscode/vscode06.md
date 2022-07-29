<!--
 * @Author: hly
 * @Date: 2022-07-29 09:00:42
 * @LastEditors: hly
 * @LastEditTime: 2022-07-29 10:04:36
 * @Description:
-->
day24

目标：搞定git

1. 显示源代码管理面板
    vscode中是 ctrl + shift +g
    通过设置改成vim操作 空格 + g + g

2. Stage change
    通过设置改成vim操作 空格 + g + s

3. commit

    通过设置改成vim操作 空格 + g + c
    ```
    // settings.json
        "vim.normalModeKeyBindingsNonRecursive": [
        // 显示源代码管理
        {
            "before": ["<Leader>", "g", "g"],
            "commands": ["workbench.view.scm"],
        },
        // Stage change
        {
            "before": ["<Leader>", "g", "s"],
            "commands": ["git.stage"],
        },
        // commit
        {
            "before": ["<Leader>", "g", "c"],
            "commands": ["git.commit"],
        },
    ],
    ```
git.stageChange
