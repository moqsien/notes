## vscode 配置（py、java、vue、golang）

---

```json

{
    "go.gopath": "/home/moqsien/projects/golang",
    "go.useGoProxyToCheckForToolUpdates": true,
    "go.useLanguageServer": true,
    // "go.alternateTools": {
    //   "gopls": "gopls"
    // },
    "go.languageServerExperimentalFeatures": {
        "diagnostics": true,
        "documentLink": true,
    },
    "go.autocompleteUnimportedPackages": true,
    "go.docsTool": "gogetdoc",
    "go.lintTool": "golangci-lint",
    "go.lintFlags": [
        "--disable=all",
        "--enable=errcheck"
    ],
    "[go]": {
        "editor.insertSpaces": false,
        "editor.formatOnSave": true,
        "editor.codeActionsOnSave": {
            "source.organizeImports": true
        }
    },
    "go.useCodeSnippetsOnFunctionSuggest": true,
    "go.editorContextMenuCommands": {
        "toggleTestFile": true,
        "addTags": true,
        "removeTags": false,
        "testAtCursor": true,
        "testFile": false,
        "testPackage": false,
        "generateTestForFunction": true,
        "generateTestForFile": false,
        "generateTestForPackage": false,
        "addImport": true,
        "testCoverage": true,
        "playground": true,
        "debugTestAtCursor": true
    },
    "editor.fontSize": 17,
    "editor.formatOnSave": true,
    "editor.formatOnType": true,
    "editor.formatOnPaste": true,
    "editor.quickSuggestionsDelay": 50,
    "editor.suggestSelection": "first",
    "editor.codeActionsOnSave": {
        "source.fixAll": true,
    },
    "files.autoSave": "onWindowChange",
    "files.exclude": {
        "**/.git": true,
        "**/.svn": true,
        "**/.hg": true,
        "**/CVS": true,
        "**/.DS_Store": true,
        "**/__pycache__": true,
        "**/*.pyc": true,
        "**/.vscode": true,
        "**/*.wpr": true,
        "**/*.wpu": true,
        "**/.idea": true
    },
    "workbench.iconTheme": "material-icon-theme",
    "kite.enableSnippets": true,
    "kite.showWelcomeNotificationOnStartup": false,
    "kite.startKiteEngineOnStartup": true,
    "kite.developerMode": true,
    "kite.enableOptionalCompletionsTriggers": true,
    "kite.showGoBetaNotification": false,
    "python.linting.enabled": true,
    "python.languageServer": "Pylance",
    "python.autoUpdateLanguageServer": false,
    "python.autoComplete.addBrackets": true,
    "python.defaultInterpreterPath": "~/.virtualenvs/web/bin/python3.8",
    "python.venvPath": "~/.virtualenvs/",
    "python.autoComplete.showAdvancedMembers": true,
    "python.formatting.autopep8Args": [
        "--max-line-length=120",
        "--experimental"
    ],
    "workbench.editor.enablePreview": false,
    "[jsonc]": {
        "editor.defaultFormatter": "vscode.json-language-features"
    },
    "terminal.external.linuxExec": "terminator",
    "code-runner.clearPreviousOutput": true,
    "code-runner.runInTerminal": true,
    "code-runner.saveFileBeforeRun": true,
    "code-runner.fileDirectoryAsCwd": true,
    "code-runner.showRunCommandInEditorContextMenu": true,
    "code-runner.preserveFocus": true,
    "code-runner.showExecutionMessage": true,
    "code-runner.executorMap": {
        "javascript": "node",
        "java": "cd $dir && javac $fileName && java $fileNameWithoutExt",
        "c": "cd $dir && gcc $fileName -o $fileNameWithoutExt && $dir$fileNameWithoutExt",
        "cpp": "cd $dir && g++ $fileName -o $fileNameWithoutExt && $dir$fileNameWithoutExt",
        "objective-c": "cd $dir && gcc -framework Cocoa $fileName -o $fileNameWithoutExt && $dir$fileNameWithoutExt",
        "python": "~/.virtualenvs/web/bin/python3.8 -u",
        "go": "go run",
        "lua": "lua",
        "shellscript": "bash",
        "typescript": "ts-node",
        "rust": "cd $dir && rustc $fileName && $dir$fileNameWithoutExt",
    },
    "breadcrumbs.enabled": true,
    "editor.renderWhitespace": "all",
    "diffEditor.ignoreTrimWhitespace": false,
    "terminal.integrated.fontSize": 16,
    "vim.easymotion": true,
    "vim.incsearch": true,
    "vim.useSystemClipboard": true,
    "vim.useCtrlKeys": true,
    "vim.hlsearch": true,
    "vim.insertModeKeyBindings": [
        {
            "before": [
                "j",
                "j"
            ],
            "after": [
                "<Esc>"
            ]
        }
    ],
    "vim.normalModeKeyBindingsNonRecursive": [
        {
            "before": [
                "<leader>",
                "d"
            ],
            "after": [
                "d",
                "d"
            ]
        },
        {
            "before": [
                "<C-n>"
            ],
            "commands": [
                ":nohl"
            ]
        }
    ],
    "vim.leader": "<space>",
    "vim.handleKeys": {
        "<C-a>": false,
        "<C-f>": false
    },
    "window.zoomLevel": 0,
    "workbench.colorTheme": "Base16 Dark Summerfruit",
    "powermode.enabled": true,
    "java.semanticHighlighting.enabled": true,
    "eslint.validate": [
        "javascript",
        "javascriptreact",
        "vue"
    ],
    "[vue]": {
        "editor.defaultFormatter": "octref.vetur",
    },
    "[javascript]": {
        "editor.defaultFormatter": "vscode.typescript-language-features",
    },
    "vetur.format.defaultFormatter.js": "vscode-typescript",
    "javascript.format.semicolons": "remove",
    "javascript.format.insertSpaceBeforeFunctionParenthesis": true,
    "explorer.confirmDelete": false,
    "glassit-linux.opacity": 95,
    "todo-tree.tree.showScanModeButton": false,
    "todo-tree.highlights.defaultHighlight": {
        "icon": "alert",
        "type": "text",
        "foreground": "red",
        "background": "white",
        "opacity": 50,
        "iconColour": "blue"
    },
    "todo-tree.highlights.customHighlight": {
        "TODO": {
            "icon": "check",
            "type": "line"{
                "workbench.colorTheme": "Tokyo Night",
                "editor.suggestSelection": "first",
                "vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",
                "workbench.iconTheme": "material-icon-theme",
                "todo-tree.tree.showScanModeButton": false
            }
        },
        "FIXME": {
            "foreground": "black",
            "iconColour": "yellow",
            "gutterIcon": true
        }
    },
    "python.analysis.completeFunctionParens": true,
}
```
