<p align="center">
	<a href="https://code.visualstudio.com">
		<img src="./icons/vscode.png" attr="rsync logo" title="官网：https://www.docker.com">
	</a>
</p>

当前版本：`v1.22.1`

最终效果预览

![Visual Studio Code](./preview.png "Visual Studio Code")

> PS：预览图中的最终效果，基于图标主题 **Material Icon Theme** 和 颜色主题 **One Monokai Theme** 定制，详见[自定义配置](./settings.json)。

### 替代图标

[点击这里预览](./icons/README.md)

### 第三方插件

- Paste and Indent

    > 带格式的粘贴

    ```
    # 1. 修改文件 keybindings.json，追加以下设置（ctrl+v 带格式；ctrl+shift+v 原样）
    [
        {
            "key": "cmd+v",
            "command": "pasteAndIndent.action",
            "when": "editorTextFocus && !editorReadonly"
        },
        {
            "key": "cmd+v",
            "command": "editor.action.clipboardPasteAction",
            "when": "!editorTextFocus"
        },
        {
            "key": "cmd+shift+v",
            "command": "editor.action.clipboardPasteAction",
            "when": "editorTextFocus && !editorReadonly"
        }
    ]
    # 2. 修改用户配置 Preferences > Settings，追加如下设置
    "pasteAndIndent.selectAfter": true,
    ```

- PHP IntelliSense

    > PHP 语法检查、提示加强等

    ```
    "php.executablePath": "/usr/local/bin/php",
    "php.suggest.basic": false,
    ```

- PHP Debug

    > PHP 断点调试，详细配置[单击这里](./php_xdebug.md)

- PHP DocBlocker

    > PHP 快速注释工具

- Bracket Pair Colorizer

    > 括号高亮

    ```
    "editor.matchBrackets": false,
    "bracketPairColorizer.highlightActiveScope": true,
    "bracketPairColorizer.activeScopeCSS": [
        "borderStyle : none",
        "backgroundColor : {color}; opacity: 0.5"
    ],
    ```

- Insert Date String

 	> 插入日期时间

 	```
    // 插入日期时间 command + shift + i
    //  DDDD, MMMM D, YYYY A HH:mm:ss -> Tuesday, April 3, 2018 PM 02:35:08
    "insertDateString.format": "YYYY/MM/DD hh:mm:ss"
 	```