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
- IntelliSense for CSS class names in HTML
- Live Server
- Path Intellisense - дополнение путей и имён файлов (+php)

- PHP Intelephense
- PHP IntelliSense

- Code Spell Checker
- Russian - Code Spell Checker

- Jekyll Syntax Support
- Liquid
- Twig Language
- laravel-blade
- Laravel Blade formatter


## Settings:

```js
{
    {
    "workbench.startupEditor": "none",
    "workbench.statusBar.visible": true,
    "workbench.activityBar.visible": true,
    "workbench.editor.tabSizing": "shrink",
    "workbench.editor.wrapTabs": true,
    "workbench.colorCustomizations": {
        "editorIndentGuide.activeBackground": "#ff0000"
    },
    "window.menuBarVisibility": "visible",
    "workbench.colorTheme": "Default Dark+",

    "security.workspace.trust.enabled": false,
    "security.workspace.trust.untrustedFiles": "open",

    "files.defaultLanguage": "html",

    "git.autofetch": true,
    "git.ignoreMissingGitWarning": true,

    // "editor.fontFamily": "Fira Code", // поддерживает лигатуры
    "editor.fontSize": 17,
    "editor.tabCompletion": "on",
    "editor.fontWeight": "100",
    "editor.fontLigatures": true,

    "editor.tabSize": 4,
    "editor.insertSpaces": true, //Вставлять пробелы при нажатии клавиши TAB
    "editor.detectIndentation": false, //Только пробелы вместо TAB
    "editor.renderWhitespace": "boundary", // Всегда показывать (..)
    "editor.folding": true,
    "editor.glyphMargin": true,
    "editor.smoothScrolling": true,
    "editor.linkedEditing": true,
    "editor.renderControlCharacters": true,
    "editor.parameterHints.enabled": false, // Всплывающая подсказка в коде
    "editor.hover.enabled": false, // Всплывающая подсказка в коде при наведении

    "terminal.integrated.defaultProfile.windows": "Ubuntu (WSL)",
    "terminal.integrated.fontSize": 16,
    "terminal.integrated.fontWeight": "100",

    "emmet.includeLanguages": {
        "javascript": "javascriptreact",
        "liquid":     "html",
        "jekyll":     "html",
    },

    // Указывает на исполняемый файл PHP.
    "php.suggest.basic": false, // откл. станд. php
    "php.validate.executablePath": "D:\\OSPanel\\modules\\php\\PHP_7.4\\php.exe", // Desktop

    // ассоциации файлов
    "files.associations": {
        "*.tpl": "php",
        "*.twig": "php",
        "*.liquid": "html",
    },
    "[php]": {
        "editor.defaultFormatter": "bmewburn.vscode-intelephense-client"
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

    "javascript.updateImportsOnFileMove.enabled": "always",
    "explorer.confirmDragAndDrop": false,

    "cSpell.language": "en,ru",
    
    "intelephense.stubs": [
        "apache",
        "bcmath",
        "bz2",
        "calendar",
        "com_dotnet",
        "Core",
        "ctype",
        "curl",
        "date",
        "dba",
        "dom",
        "enchant",
        "exif",
        "FFI",
        "fileinfo",
        "filter",
        "fpm",
        "ftp",
        "gd",
        "gettext",
        "gmp",
        "hash",
        "iconv",
        "imap",
        "intl",
        "json",
        "ldap",
        "libxml",
        "mbstring",
        "meta",
        "mysqli",
        "oci8",
        "odbc",
        "openssl",
        "pcntl",
        "pcre",
        "PDO",
        "pdo_ibm",
        "pdo_mysql",
        "pdo_pgsql",
        "pdo_sqlite",
        "pgsql",
        "Phar",
        "posix",
        "pspell",
        "readline",
        "Reflection",
        "session",
        "shmop",
        "SimpleXML",
        "snmp",
        "soap",
        "sockets",
        "sodium",
        "SPL",
        "sqlite3",
        "standard",
        "superglobals",
        "sysvmsg",
        "sysvsem",
        "sysvshm",
        "tidy",
        "tokenizer",
        "xml",
        "xmlreader",
        "xmlrpc",
        "xmlwriter",
        "xsl",
        "Zend OPcache",
        "zip",
        "zlib",
        "wordpress"
    ],
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
            "    <img src='./assets/img/desktop' alt='alt'>",
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
    // javascript:void(0);
    "void-js": {
        "scope": "html, php",
        "prefix": "void",
        "body": [
            "javascript:void(0);"
        ],
        "description": "javascript:void(0);"
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

### exclude folders

```json
"search.exclude": {
    "**/ARM/library/**": true
},
"php.problems.exclude": {
    "/" : [437], // exclude $this error
    "**/ARM/library/**": true
},
```
