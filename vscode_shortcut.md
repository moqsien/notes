### vscode 快捷键配置
```json
// 将键绑定放在此文件中以覆盖默认值auto[]
[
    {
        "command": "vscode-neovim.compositeEscape1",
        "key": "j",
        "when": "neovim.mode == insert && editorTextFocus",
        "args": "j"
    },
    {
        "key": "cmd+g c",
        "command": "workbench.action.showCommands"
    },
    {
        "key": "cmd+g s",
        "command": "workbench.action.openSettings"
    },
    {
        "key": "cmd+g k",
        "command": "workbench.action.openGlobalKeybindings"
    },
    {
        "key": "cmd+g d",
        "command": "workbench.action.files.openFolder"
    },
    {
        "key": "cmd+g f",
        "command": "workbench.action.files.openFile"
    },
    {
        "key": "cmd+g r",
        "command": "workbench.action.openRecent"
    },
    {
        "key": "cmd+g n",
        "command": "workbench.action.newWindow"
    },
    {
        "key": "cmd+g q",
        "command": "workbench.action.closeWindow"
    },
    {
        "key": "cmd+f n",
        "command": "welcome.showNewFileEntries"
    },
    {
        "key": "cmd+f o",
        "command": "workbench.action.files.openFileFolder"
    },
    {
        "key": "cmd+f a",
        "command": "workbench.action.files.saveAs"
    },
    {
        "key": "cmd+f s",
        "command": "workbench.action.files.save"
    },
    {
        "key": "cmd+f w",
        "command": "workbench.action.files.saveAll"
    },
    {
        "key": "cmd+f q",
        "command": "workbench.action.closeActiveEditor"
    },
    {
        "key": "cmd+f c",
        "command": "workbench.action.closeAllEditors"
    },
    {
        "key": "cmd+f l",
        "command": "codelens.showLensesInCurrentLine"
    },
    {
        "key": "cmd+n u",
        "command": "workbench.action.toggleSidebarVisibility"
    },
    {
        "key": "cmd+n f",
        "command": "workbench.action.replaceInFiles"
    },
    {
        "key": "cmd+n d",
        "command": "workbench.action.debug.start",
        "when": "viewContainer.workbench.view.debug.enabled"
    },
    {
        "key": "cmd+n g",
        "command": "workbench.view.scm",
        "when": "workbench.scm.active"
    },
    {
        "key": "cmd+n x",
        "command": "workbench.view.extensions",
        "when": "viewContainer.workbench.view.extensions.enabled"
    },
    {
        "key": "cmd+n t",
        "command": "todo-tree-view.focus"
    },
    {
        "key": "cmd+n p",
        "command": "workbench.view.extension.project-manager"
    },
    {
        "key": "cmd+n s",
        "command": "projectManager.saveProject"
    },
    {
        "key": "cmd+n e",
        "command": "workbench.files.action.focusFilesExplorer"
    },
    {
        "key": "cmd+n n",
        "command": "workbench.view.extension.easynotesView"
    },
    {
        "key": "cmd+p t",
        "command": "workbench.action.terminal.toggleTerminal",
        // "when": "terminal.active"
    },
    {
        "key": "cmd+p o",
        "command": "workbench.action.output.toggleOutput",
        // "when": "workbench.panel.output.active"
    },
    {
        "key": "cmd+p m",
        "command": "workbench.action.problems.focus",
    },
    {
        "key": "cmd+p p",
        "command": "workbench.action.togglePanel"
    },
    {
        "key": "ctrl+alt+cmd+t",
        "command": "workbench.action.terminal.new",
        "when": "terminalProcessSupported || terminalWebExtensionContributedProfile"
    },
    {
        "key": "ctrl+9",
        "command": "editor.debug.action.toggleBreakpoint",
        "when": "debuggersAvailable && editorTextFocus"
    },
    {
        "key": "f9",
        "command": "-editor.debug.action.toggleBreakpoint",
        "when": "debuggersAvailable && editorTextFocus"
    },
    {
        "key": "ctrl+8",
        "command": "workbench.action.debug.start",
        "when": "debuggersAvailable && debugState == 'inactive'"
    },
    {
        "key": "f5",
        "command": "-workbench.action.debug.start",
        "when": "debuggersAvailable && debugState == 'inactive'"
    }
]
```