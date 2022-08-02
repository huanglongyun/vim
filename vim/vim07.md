day7

目标：在单文件中移动的更快

1. 滚动
    1. 向下滚动一屏 ctrl - f (forward)
    2. 向上滚动一屏 ctrl - b (backward)
    3. 向下滚动半屏 ctrl - d
    4. 向上滚动半屏 ctrl - u
    5. 向下滚动一行 ctrl - e
    6. 向上滚动一行 ctrl - y
    7. 基于配置（更容易记忆）
        1. 上5行 shift - k (即大写 K)
        2. 下5行 shift - j （即大写 J）
        配置
            1. normal

                    "vim.visualModeKeyBindings": [
                        {
                            "before":["J"],
                            "after":["5","j"]
                        },

                        {
                            "before":["K"],
                            "after":["5","k"]
                        }
                    ],
            2. visual

                    "vim.normalModeKeyBindings": [
                        {
                            "before":["J"],
                            "after":["5","j"]
                        },

                        {
                            "before":["K"],
                            "after":["5","k"]
                        }
                    ],

2. 将当前行置于屏幕中央 zz
3. 将当前行置于屏幕顶部附近 zt (top)
4. 将当前行置于屏幕底部附近 zb (bottom)
5. 跳到文件首 gg
6. 跳到文件尾 G
7. 跳到指定行
    1. 行数 + gg
    2. 行数 + G

感觉较有用都是 ctrl-f ctrl-b K J zz gg G