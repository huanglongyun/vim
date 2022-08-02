<!--
 * @Author: hly
 * @Date: 2022-07-27 08:31:01
 * @LastEditors: hly
 * @LastEditTime: 2022-07-28 09:02:15
 * @Description:
-->
day22

目标：编码

命令优先级：效率高，优先级就高

1. ctrl + .
    显示提示
    show code actions
    不生效的话，可能被搜狗输入法影响了， 更多设置=>属性设置=>按键=>中英标点切换 ctrl + 句号，将其关掉就好

2. ctrl + shift + space
    触发函数参数提示
    Trigger parameter hints

3. ctrl + i
    触发建议
    Trigger suggestion
    ```
        // settings.json
        "vim.handleKeys": {
            "<C-i>": false,
        },
    ```
4. alt + up/down
    移动行

5. ctrl + enter
    增加行（向下增加）
    ctrl + shift + enter 向上添加一行，不生效

6. 删除前面的单词 不生效
    opt + delete
    opt + ctrl + delete 基于单词删除，如驼峰命名的，会根据单词删除

7. f8 跳转到错误处(向下跳转)
    shift + f8 向上跳转到错误处

9. ctrl + f2
    选择所有出现的当前单词

