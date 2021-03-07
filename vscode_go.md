- golang安装
  - 下载
  ```text
  https://golang.google.cn/dl/
  ```
  - 安装
  ```text
  解压后将go文件夹mv到/usr/local
  在/etc/profile中配置环境变量，参考以下示例：
  export GOROOT="/usr/local/go"
  export PATH=$PATH:/usr/local/go/bin
  export GOPATH="/home/moqsien/Documents/projects/golang"
  export GO111MODULE=on
  export GOPROXY=https://goproxy.cn
  环境变量在/etc/profile中配置，主要是为了GOPROXY能在全局都可用，尤其是vscode自动下载工具插件时，即使不从命令行启动，也能获取到GOPROXY变量
  ```
  - 测试
  ```bash
  # 测试是否安装成功
  source /etc/profile
  go version
  ```
- vscode配置
  - go插件
  ```text
  https://marketplace.visualstudio.com/items?itemName=golang.Go#customization
  https://github.com/golang/vscode-go/blob/master/docs/settings.md
  ```
  - 配置
  ```json
  {
    "go.gopath": "/home/moqsien/projects/golang",
    "go.toolsManagement.checkForUpdates": "proxy",
    "go.useLanguageServer": true,
    "go.lintTool": "golangci-lint",
    "go.lintFlags": [
        "--disable-all",
        "--enable golint"
    ],
    "go.formatTool": "goimports",
    "go.languageServerExperimentalFeatures": {
        "diagnostics": true
    },
    "go.useCodeSnippetsOnFunctionSuggest": true,
    "go.editorContextMenuCommands": {
        "toggleTestFile": true,
        "addTags": true,
        "removeTags": false,
        "fillStruct": false,
        "testAtCursor": true,
        "testFile": false,
        "testPackage": false,
        "generateTestForFunction": true,
        "generateTestForFile": false,
        "generateTestForPackage": false,
        "addImport": true,
        "testCoverage": true,
        "playground": true,
        "debugTestAtCursor": true,
        "benchmarkAtCursor": false
    },
    "[go]": {
        "editor.autoIndent": "full",
        "editor.fontSize": 16
    },
    "gopls": {
        // 导包不会当作url
        "ui.navigation.importShortcut": "Definition",
        "ui.documentation.hoverKind": "SynopsisDocumentation"
    },
    "go.toolsManagement.autoUpdate": true,
  }
  ```