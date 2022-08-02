<!--
 * @Author: hly
 * @Date: 2022-08-01 08:31:05
 * @LastEditors: hly
 * @LastEditTime: 2022-08-01 09:49:46
 * @Description:
-->
day26

目标 snippets 代码片段

快速创建代码模板，减少重复性劳动，提升开发效率，也有逼格

1. 安装插件
    JavaScript (ES6) code snippets
    Vue 3 Snippets
    Vue VSCode Snippets
    JavaScript standardjs styled snippets

2. 使用
    imp => import second from 'first'
    imd => import { second } from 'first'
    fn => function name (arguments) {}
    log => console.log();

    andn => (params) => {}
    iife => ;(function (arguments) {})()
    rp => return new Promise((resolve, reject) => {})
3. 技巧
    tab键可以切换位置
    如果不小心取消提示时用 => ctrl + i

4. 自己写一个
    1. 开发文档
        https://code.visualstudio.com/docs/editor/userdefinedsnippets
        https://snippet-generator.app/

        VSCode 命令栏搜 user snippets 可选择创建全局的,也可以基于语言设置。

    2. 知识点
        1. tab位置
            使用tab，可以使编辑器光标在代码片段中移动。
            使用 $1、 $2指定光标位置。这个数字是访问制表位的顺序，
            而 $0表示最终的光标位置
        2. 默认值 ${1:foo}
        3. 多选 ${1|one,two,three|}
        4. 变量 $name https://code.visualstudio.com/docs/editor/userdefinedsnippets#_variables
    3. 例子

