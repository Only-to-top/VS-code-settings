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

<li>Swig(.tpl)    // .tpl синтаксис</li>
</ul>



<h2>Settings:</h2>

```js
{
  "workbench.startupEditor": "none", //редактор при запуске
  "workbench.statusBar.visible": true,
  "workbench.activityBar.visible": true,
  "workbench.statusBar.feedback.visible": false,
  "workbench.editor.tabSizing": "shrink",
  "workbench.colorCustomizations": {
    "editorIndentGuide.activeBackground": "#ff0000"
  },
  "window.zoomLevel": 0,
  "window.menuBarVisibility": "visible",
  "git.ignoreMissingGitWarning": true,
  "files.defaultLanguage": "html",
  "editor.fontSize": 17,

  "editor.tabSize": 2,
  "editor.insertSpaces": true, //Вставлять пробелы при нажатии клавиши TAB
  "editor.detectIndentation": false, //Только пробелы вместо TAB
  "editor.renderWhitespace": "boundary", //отбражение пробелов

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
  "liveSassCompile.settings.generateMap": false,
  "liveSassCompile.settings.formats": [
    {
      "format": "expanded",
      "extensionName": ".css",
      "savePath": "/css/"
    }
  ],

  // Путь к исполняемому файлу Git с именем исполняемого файла Git
  "git.path": "C:\\Program Files\\Git\\bin\\git.exe",

  // Указывает на исполняемый файл PHP.
  "php.suggest.basic": false, // откл. станд. php
  "php.validate.executablePath": "D:\\OSPanel\\modules\\php\\PHP_7.1-x64\\php.exe",
  // "php.validate.executablePath": "D:\\www\\OSPanel\\modules\\php\\PHP_7.1-x64\\php.exe",

}
```

<h2>Фрагменты кода пользователя:</h2>

```js
{
  "Print to console": {
    "prefix": "media",
    "scope": "sass",
    "body": "@media only screen and (max-width : 1200px)",
    "description": "Вставить медиа запрос"
  }
}

{
  "Print to console": {
    "prefix": "@media",
    "scope": "css",
    "body": [
      "@media only screen and (max-width: 768px) {",
      "$1",
      "}"
    ],
    "description": "Вставить медиа запрос"
  }
}

// php.json
{
  "@media": {
    "prefix": "print",
    "body": [
      "echo '<pre>';",
      "print_r($1);",
      "echo '</pre>';"
    ],
    "description": "Вставить print_r"
  }
}
```


<h2>Hot Keys:</h2>

```js
{
  "key": "ctrl+shift+g",
  "command": "editor.emmet.action.wrapWithAbbreviation"
}
```
