# Settings  VS Code

## Extensions:

- Apache Conf
- Auto Close Tag
- Auto Rename Tag
- AutoFileName
- Bracket Pair Colorizer
- Color Highlight
- CSS Formatter
- Highlight Matching Tag
- Indenticator
- HTML CSS Support
- JavaScript (ES6) code snippets
- Liquid
- Jekyll Syntax Support
- Live Sass Complier
- Live Server
- Material Theme
- Path Intellisense - дополнение путей и имён файлов (+php)
- PHP Intelephense
- PHP IntelliSense
- Remote - WSL
- Sass


## Settings:

```js
{
    "workbench.startupEditor": "none",
    "workbench.statusBar.visible": true,
    "workbench.activityBar.visible": true,
    "workbench.editor.tabSizing": "shrink",
    "workbench.colorCustomizations": {
        "editorIndentGuide.activeBackground": "#ff0000"
    },

    "window.zoomLevel": 0,
    "window.menuBarVisibility": "visible",

    "git.autofetch": true,
    "git.ignoreMissingGitWarning": true,

    "files.defaultLanguage": "html",

    "editor.fontSize": 16,
    "editor.tabCompletion": "on",
    "editor.fontFamily": "Fira Code", // поддерживает лигатуры
    "editor.fontWeight": "100",
    "editor.fontLigatures": true,

    "editor.tabSize": 4,
    "editor.insertSpaces": true, //Вставлять пробелы при нажатии клавиши TAB
    "editor.detectIndentation": false, //Только пробелы вместо TAB
    "editor.renderWhitespace": "boundary",
    "editor.folding": true,
    "editor.glyphMargin": true,
    "editor.smoothScrolling": true,

    "terminal.integrated.shell.windows": "C:\\Windows\\System32\\bash.exe",
    "terminal.integrated.rendererType": "dom",
    "terminal.integrated.fontWeight": "100",

    // highlight-matching-tag
    "highlight-matching-tag.styles": {
        "opening": {
            "left": {
                "custom": {
                    "borderWidth": "2px 2px 2px 2px",
                    "borderStyle": "solid",
                    "borderColor": "yellow",
                    "borderRadius": "5px"
                }
            },
            "right": {
                "custom": {
                    "borderWidth": "2px 2px 2px 2px",
                    "borderStyle": "solid",
                    "borderColor": "yellow",
                    "borderRadius": "5px"
                }
            }
        }
    },
    
    // liveServer
    "liveServer.settings.donotVerifyTags": true,
    "liveServer.settings.donotShowInfoMsg": true,

    // liveSassCompiler
    "liveSassCompile.settings.formats": [{
        "format": "expanded",
        "extensionName": ".css",
        "savePath": "/assets/css/"
    }],

    "javascript.updateImportsOnFileMove.enabled": "always",
    "explorer.confirmDragAndDrop": false,
    "editor.renameOnType": true,
    "workbench.colorTheme": "Community Material Theme Darker High Contrast",

    // Указывает на исполняемый файл PHP.
    "php.suggest.basic": false, // откл. станд. php
    "php.validate.executablePath": "D:\\OSPanel\\modules\\php\\PHP_7.3\\php.exe", // Desktop
    // "php.validate.executablePath": "D:\\web\\OSPanel\\modules\\php\\PHP-7.1-x64\\php.exe", // Notebook

    "emmet.includeLanguages": {
        "javascript": "javascriptreact",
        "liquid":     "html",
        "jekyll":     "html",
    },

    // ассоциации файлов
    "files.associations": {
        "*.tpl": "php",
        "*.twig": "php",
        "*.liquid": "html",
    },
    "[php]": {
        "editor.defaultFormatter": "bmewburn.vscode-intelephense-client"
    },

}
```


## User snippets GLOBAL:

```js
{
    // sass media
    "@media SASS": {
        "prefix": "@media",
        "scope": "sass",
        "body": [
            "@media only screen and (max-width : $1px)",
            "$2"
        ],
        "description": "Вставить медиа запрос"
    },
    // css media
    "@media CSS": {
        "prefix": "@media",
        "scope": "css",
        "body": [
            "@media only screen and (max-width: $1px) {",
            "$2",
            "}"
        ],
        "description": "Вставить медиа запрос"
    },
    // print_r beautiful on PHP
    "@media": {
        "prefix": "print",
        "scope": "php",
        "body": "echo '<pre>' . print_r($$1, true) . '</pre>';",
        "description": "Вставить print_r"
    },
    // HTML start template
    "!html": {
        "prefix": "!html",
        "scope": "html",
        "body": [
            "<!DOCTYPE html>",
            "<html lang='ru'>",
            "<head>",
            "   <meta charset='UTF-8'>",
            "   <meta name='viewport' content='width=device-width, initial-scale=1.0'>",
            "   <meta http-equiv='X-UA-Compatible' content='ie=edge'>",
            "   <title>$1</title>",
            "   <link rel='stylesheet' href='https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css'>",
            "</head>",
            "<body>",
            "",
            "$2",
            "",
            "<script src='https://code.jquery.com/jquery-3.4.1.min.js'></script>",
            "</body>",
            "</html>"
        ],
        "description": "HTML start tpl"
    },
    // highlight Jekyll
    "highlight": {
        "prefix": "high",
        "scope": "html, liquid, jekyll",
        "body": [
            "{% highlight $1 %}",
            "$2",
            "{% endhighlight %}"
        ],
        "description": "Вставить highlight"
    },
    // rel nofollow
    "rel=nofollow": {
        "prefix": "rel",
        "scope": "html, liquid, jekyll",
        "body": [
            "rel='nofollow noopener noreferrer'"
        ],
        "description": "Вставить rel='nofollow'"
    },
    // <picture> WEBP
    "picture-WEBP": {
        "prefix": "picture",
        "scope": "html, liquid, jekyll",
        "body": [
            "<picture itemscope itemtype='http://schema.org/ImageObject'>",
            "   <source srcset='img/image.webp' type='image/webp'>",
            "   <img",
            "       itemprop='contentUrl'",
            "       src='img/image.jpg'",
            "       alt='alt'",
            "       class='img-responsive'",
            "   >",
            "</picture>"
        ],
        "description": "Вставить WEBP изображение"
    },
    // <picture> Schema
    "picture-microdata": {
        "prefix": "picture",
        "scope": "html, liquid, jekyll",
        "body": [
            "<picture itemscope itemtype='http://schema.org/ImageObject'>",
            "   <img",
            "       itemprop='contentUrl'",
            "       src='img/image.jpg'",
            "       alt='alt'",
            "       class='img-responsive'",
            "   >",
            "</picture>"
        ],
        "description": "Вставить Микроразметку картинки"
    },
    // <picture> media
    "picture-media": {
        "prefix": "picture",
        "scope": "html, liquid, jekyll",
        "body": [
            "<picture>",
            "    <source media='(max-width: 576px)' srcset='./assets/img/mobile'>",
            "    <source media='(min-width: 577px)' srcset='./assets/img/desktop'>",
            "    <img src='' alt=''>",
            "</picture>"
        ],
        "description": "Вставить media изображение"
    },
    // span.ground
    "span.ground": {
        "prefix": "sgr",
        "scope": "html, liquid, jekyll",
        "body": [
            "<span class='ground'>$1</span>"
        ],
        "description": "Вставить WEBP изображение"
    },
    // grid-tml columns
    "Grid-template-columns": {
        "scope": "sass,css",
        "prefix": "gtc",
        "body": [
            "grid-template-columns: repeat(auto-fill, minmax(130px, 1fr));"
        ],
        "description": "Грид шаблон колонок"
    },
    // log openCart
    "Log-write": {
        "scope": "php",
        "prefix": "log",
        "body": [
            "\\$this->log->write($1);"
        ],
        "description": "Вывод в журнал ошибок"
    },
    // Clamp secure
    "Clamp-function": {
        "scope": "css",
        "prefix": "clamp",
        "body": [
            "min(max($1, $2), $3);"
        ],
        "description": "Clamp безопасный"
    },
}
```


## Hot Keys:

```js
{
    "key": "ctrl+shift+g",
    "command": "editor.emmet.action.wrapWithAbbreviation"
}
```
