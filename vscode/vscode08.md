<!--
 * @Author: hly
 * @Date: 2022-08-02 08:36:00
 * @LastEditors: hly
 * @LastEditTime: 2022-08-02 10:46:06
 * @Description:
-->
day27

目标：掌握重构

1. 装插件，和寻找到满足自己需求的插件
2. 使用 ctrl + . 找到自己所需要的功能
3. 较常用的还可以自定义快捷键

1. vscode自带
    1. 提示
        1. ctrl + shift + r 只会出现和重构相关的提示
        2. ctrl + . 出现所有提示
    2. 文档 https://code.visualstudio.com/docs/typescript/typescript-refactoring
    3. Extract Method 提炼方法
    4. Extract Variable 提炼变量
    5. 重命名 空格 + r + n

2. 插件 Abracadabra https://marketplace.visualstudio.com/items?itemName=nicoespeon.abracadabra
    提炼变量
    转换模板字符串

3. 插件 Hocus Pocus https://marketplace.visualstudio.com/items?itemName=nicoespeon.hocus-pocus
    创建函数
        先写函数（如：fn()),然后使用插件
        1. ctrl + . 提示选择
        2. 设置快捷键 空格 + f + f
    创建变量

        设置快捷键 空格 + v + v
    ```
    // settings.json
        "vim.normalModeKeyBindingsNonRecursive": [
            // 插件Hocus Pocus 快捷键 创建变量
            {
                "before":["<Leader>", "v","v"],
                "commands":["hocusPocus.createVariable"]
            },
            // 插件Hocus Pocus 快捷键 创建函数
            {
                "before":["<Leader>", "f","f"],
                "commands":["hocusPocus.createFunction"]
            }
        ],
    ```
4. 插件 JavaScript Booster https://marketplace.visualstudio.com/items?itemName=sburg.vscode-javascript-booster
    和Abracadabra
    箭头函数转换
    三目运算符转换