<!--
 * @Author: hly
 * @Date: 2022-07-11 09:26:13
 * @LastEditors: hly
 * @LastEditTime: 2022-07-11 11:24:45
 * @Description:
-->
day9

目标：更高效的移动，想去哪里就去哪里

1. 插件一 vim-easymotion
    直接高亮匹配项并将它们临时用不同字母替换，按下相应字母后跳转到相应位置然后取消替换，提供强化版的检索式移动
    配置：vscode中setting.json配置
    ```
        "vim.easymotion": true, // 开启插件
        "vim.leader": "<Space>", // leader 默认的是 \\ 但较远不好按，改成 space（空格）代替
    ```
    <leader> 等于 空格
    Start of word forwards. <leader><leader> w 向下单词头部
    Start of word backforwards. <leader><leader> b 向上单词头部
    End of word forwards. <leader><leader> e 向下单词尾部
    End of word backforwards. <leader><leader> ge 向上单词尾部
    Start of line forwards. <leader><leader> j 向下 行
    Start of line backwards <leader><leader> k 向上 行
    Matches beginning & ending of word,camelCase, after _, and after # forwards <leader><leader> l
    Matches beginning & ending of word,camelCase, after _, and after # backwards <leader><leader> h
    JumpToAnywhere motion; default behavior matches beginning & ending of word, camelCase, after _ and after # <leader><leader> <leader> j

2. 插件 vim-sneak
    s + 2个字符
    配置：vscode中setting.json配置
    ```
    "vim.sneak": true,
    ```
    改键:替换原生的f 功能
    ```
        "vim.normalModeKeyBindingsNonRecursive": [
      {
        "before":["f"],
        "after":["s"]
      },
      {
        "before":["F"],
        "after":["S"]
      },
      {
        "before":["s"],
        "after":["c", "l"]
      },
      {
        "before":["S"],
        "after":["^", "C"]
      }
    ],
    // 可视化模式
        "vim.visualModeKeyBindingsNonRecursive": [
      {
        "before":["f"],
        "after":["s"]
      }
    ],
    // 大写S 无效果，不用改

        "vim.operatorPendingModeKeyBindingsNonRecursive": [
      {
        "before":["f"],
        "after":["z"]
      },
      {
        "before":["F"],
        "after":["Z"]
      }
    ],
```
    改键后，各模式都统一用 f 操作


    s 删除当前字符
    S 删除当前行

    重复命令 ;
    反向重复命令 ,

    ctrl r 恢复