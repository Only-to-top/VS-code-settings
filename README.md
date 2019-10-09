# Settings  VS Code

<h2>Extensions:</h2>

<ul>
  <li>Sass</li>
  <li>Live Server</li>
  <li>Live Sass Complier</li>
  <li>Highlight Matching Tag</li>
  <li>Color Highlight</li>
  <li>All Autocomplete or Path Autocomplete</li>
  <li>Apache Conf</li>
  <li>Russian Language Pack</li>
  
  <li>Dark++ Regular</li>
  <li>Material Theme</li>
</ul>



<h2>Settings:</h2>

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
    "git.ignoreMissingGitWarning": true,
    "files.defaultLanguage": "html",
    "editor.fontSize": 16,
    "editor.tabCompletion": "on", //Сниппет после нажатия TAB

    // need 'Dark++ Regular' theme
    "editor.fontFamily": "'Fira Code'", // поддерживает лигатуры
    "editor.fontWeight": "100",
    "editor.fontLigatures": true,
    "terminal.integrated.fontWeight": "100",

    "editor.tabSize": 4,
    "editor.insertSpaces": true, //Вставлять пробелы при нажатии клавиши TAB
    "editor.detectIndentation": false, //Только пробелы вместо TAB
    "editor.renderWhitespace": "boundary",

    "editor.folding": true,
    "editor.glyphMargin": true,
    "editor.smoothScrolling": true,

    "terminal.integrated.shell.windows": "C:\\Windows\\System32\\bash.exe",
    "terminal.integrated.rendererType": "dom",

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
    "liveSassCompile.settings.formats": [
        {
            "format": "expanded",
            "extensionName": ".css",
            "savePath": "/css/"
        }
    ],

  // Указываем на исполняемый файл PHP.
    "php.suggest.basic": false, // откл. станд. php
    "php.validate.executablePath": "D:\\OSPanel\\modules\\php\\PHP_7.3\\php.exe", // Desktop
    // "php.validate.executablePath": "D:\\web\\OSPanel\\modules\\php\\PHP-7.1-x64\\php.exe", // Notebook

    "workbench.colorTheme": "Material Theme Darker High Contrast",

}
```

<h2>User snippets GLOBAL:</h2>

```js
{
  // sass media
  "@media SASS": {
    "prefix": "@media",
    "scope": "sass",
    "body": [
      "@media only screen and (max-width : $1px)",
      "  $2"
    ],
    "description": "Вставить медиа запрос"
  },

  // css media
  "@media CSS": {
    "prefix": "@media",
    "scope": "css",
    "body": [
      "@media only screen and (max-width: 768px) {",
      "$1",
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

}
```


<h2>Hot Keys:</h2>

```js
{
  "key": "ctrl+shift+g",
  "command": "editor.emmet.action.wrapWithAbbreviation"
}
```
