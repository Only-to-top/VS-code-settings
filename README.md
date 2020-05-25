# Settings  VS Code

## Extensions:

- Live Server
- Sass
- Live Sass Complier
- Highlight Matching Tag
- Auto Rename Tag
- Auto Complete Tag
- Color Highlight
- Bracket Pair Colorizer
- Apache Conf
- Import Cost
- Russian Language Pack
- Material Theme


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

    // ассоциации файлов
    "files.associations": {
        "*.tpl": "php",
    },
    
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

    // Указывает на исполняемый файл PHP.
    "php.suggest.basic": false, // откл. станд. php
    "php.validate.executablePath": "D:\\OSPanel\\modules\\php\\PHP_7.3\\php.exe", // Desktop
    // "php.validate.executablePath": "D:\\web\\OSPanel\\modules\\php\\PHP-7.1-x64\\php.exe", // Notebook

    "emmet.includeLanguages": {
        "javascript": "javascriptreact",
        "liquid":     "html"
    },
    // "[html]": { "editor.formatOnSave": true },
    // "[php]": { "editor.formatOnSave": true },
    // "[javascript]": { "editor.formatOnSave": true },

    "javascript.updateImportsOnFileMove.enabled": "always",
    "explorer.confirmDragAndDrop": false,

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
        "scope": "html",
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
        "scope": "html",
        "body": [
            "rel='nofollow noopener noreferrer'"
        ],
        "description": "Вставить rel='nofollow'"
    },


    // <picture> WEBP
    "picture-WEBP": {
        "prefix": "picture",
        "scope": "html",
        "body": [
            "<picture itemscope itemtype='http://schema.org/ImageObject'>",
            "   <source srcset='img/image.webp' type='image/webp'>",
            "   <source srcset='img/image.jpg' type='image/jpeg'>",
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


    // <picture> media
    "picture-media": {
        "prefix": "picture",
        "scope": "html, liquid",
        "body": [
            "<picture>",
            "    <source media='(max-width: 576px)' srcset='./assets/img/mobile'>",
            "    <source media='(min-width: 577px)' srcset='./assets/img/desktop'>",
            "    <img src='' alt='./assets/img/desktop'>",
            "</picture>"
        ],
        "description": "Вставить media изображение"
    },


    // span.ground
    "span.ground": {
        "prefix": "sgr",
        "scope": "html",
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
            "grid-template-columns: repeat(auto-fill, minmax(130px, 1fr))"
        ],
        "description": "Грид шаблон колонок"
    }

}
```


## Hot Keys:

```js
{
    "key": "ctrl+shift+g",
    "command": "editor.emmet.action.wrapWithAbbreviation"
}
```
