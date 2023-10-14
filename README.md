# VSCODE VIM CONFIG

## vscode default shortcut

### Windows

|       key       | description               |
| :-------------: | :------------------------ |
|    **cmd+j**    | Toggle Panel              |
|    **cmd+b**    | Toggle sidebar visibility |
|   **cmd+k z**   | Toggle Zen mode           |
|   **cmd+k e**   | Focus openEditor          |
|    **cmd+-**    | Zoom In/Out               |
|    **cmd+w**    | Close window              |
| **cmd+numpad0** | Zoom Reset                |
| **shift+cmd+m** | View problems             |
| **shift+cmd+d** | View debug                |
| **shift+cmd+x** | View extensions           |
| **shift+cmd+e** | View explorer             |
| **shift+cmd+f** | View search               |

### Markdown

|     key     | description |
| :---------: | :---------- |
|  **cmd+b**  | Toggle Bold |
| **cmd+k v** | Preview     |

### Plantuml

|    key    | description |
| :-------: | :---------- |
| **alt+d** | Preview     |

## custom configuration

part of setting.json

```json
{
 /* VIM Configuration start */
  "vim.easymotion": true,
  "vim.incsearch": true,
  "vim.autoindent": true,
  "vim.useSystemClipboard": true,
  "vim.useCtrlKeys": true,
  "vim.hlsearch": true,
  "vim.insertModeKeyBindings": [
    {
      "before": ["j", "j"],
      "after": ["<Esc>"]
    }
  ],
  "vim.normalModeKeyBindingsNonRecursive": [
    {
      "before": ["<leader>", "d"],
      "after": ["d", "d"]
    },
    {
      "before": ["<C-n>"],
      "commands": [":nohl"]
    },
    {
      "before": ["<leader>", "n"],
      "commands": ["revealInExplorer"]
    },
    {
      "before": ["<leader>", "o"],
      "commands": ["workbench.action.quickOpen"]
    },
    {
      "before": ["<leader>", "c"],
      "commands": ["editor.action.commentLine"]
    },
    {
      "before": ["<leader>", "e"],
      "commands": ["workbench.explorer.fileView.focus"]
    },
    {
      "before": ["<Leader>", "f", "e"],
      "commands": ["workbench.action.files.newUntitledFile"]
    },
    {
      "before": ["<Leader>", "f", "n"],
      "commands": ["workbench.action.nextEditor"]
    },
    {
      "before": ["<Leader>", "f", "p"],
      "commands": ["workbench.action.previousEditor"]
    },
    {
      "before": ["<leader>", "f", "d"],
      "commands": ["editor.action.formatDocument"]
    },
    {
      "before": ["<Leader>", "q"],
      "commands": ["workbench.action.closeActiveEditor"]
    },
    {
      "before": ["<Leader>", "w"],
      "commands": ["workbench.action.files.save"]
    },
    {
      "before": ["<Leader>", "t", "s"],
      "commands": ["workbench.action.gotoSymbol"]
    },
    {
      "before": ["<Leader>", "p"],
      "commands": ["workbench.action.showCommands"]
    },
    {
      "before": ["<Leader>", "w", "w"],
      "commands": ["editor.action.toggleWordWrap"]
    },
    /* change view size */
    {
      "before": ["<Leader>", "v", "i", "i"],
      "commands": ["workbench.action.increaseViewSize"]
    },
    {
      "before": ["<Leader>", "v", "d", "d"],
      "commands": ["workbench.action.decreaseViewSize"]
    },
    {
      "before": ["<Leader>", "v", "i", "h"],
      "commands": ["workbench.action.increaseViewHeight"]
    },
    {
      "before": ["<Leader>", "v", "d", "h"],
      "commands": ["workbench.action.decreaseViewHeight"]
    },
    {
      "before": ["<Leader>", "v", "i", "w"],
      "commands": ["workbench.action.increaseViewWidth"]
    },
    {
      "before": ["<Leader>", "v", "d", "w"],
      "commands": ["workbench.action.decreaseViewWidth"]
    },
    /* move active editor group to up or down or left or right group*/
    {
      "before": ["<Leader>", "v", "g", "j"],
      "commands": ["workbench.action.moveActiveEditorGroupDown"]
    },
    {
      "before": ["<Leader>", "v", "g", "h"],
      "commands": ["workbench.action.moveActiveEditorGroupLeft"]
    },
    {
      "before": ["<Leader>", "v", "g", "l"],
      "commands": ["workbench.action.moveActiveEditorGroupRight"]
    },
    {
      "before": ["<Leader>", "v", "g", "k"],
      "commands": ["workbench.action.moveActiveEditorGroupUp"]
    },
    /* move current editor to first or last or next or previous group*/
    {
      "before": ["<Leader>", "v", "i", "f"],
      "commands": ["workbench.action.moveEditorToFirstGroup"]
    },
    {
      "before": ["<Leader>", "v", "i", "l"],
      "commands": ["workbench.action.moveEditorToLastGroup"]
    },
    {
      "before": ["<Leader>", "v", "i", "n"],
      "commands": ["workbench.action.moveEditorToNextGroup"]
    },
    {
      "before": ["<Leader>", "v", "i", "p"],
      "commands": ["workbench.action.moveEditorToPreviousGroup"]
    },
    /* move current editor to left or right group*/
    {
      "before": ["<Leader>", "v", "e", "h"],
      "commands": ["workbench.action.moveEditorLeftInGroup"]
    },
    {
      "before": ["<Leader>", "v", "e", "l"],
      "commands": ["workbench.action.moveEditorRightInGroup"]
    },
    /* close editor group actions*/
    {
      "before": ["<Leader>", "c", "e", "g"],
      "commands": ["workbench.action.closeEditorsAndGroup"]
    },
    {
      "before": ["<Leader>", "c", "o", "e"],
      "commands": ["workbench.action.closeOtherEditors"]
    },
    {
      "before": ["<Leader>", "c", "e", "o"],
      "commands": ["workbench.action.closeEditorsInOtherGroups"]
    },
    /* split current editor to l,h,j,k */
    {
      "before": ["<Leader>", "s", "h"],
      "commands": ["workbench.action.splitEditorLeft"]
    },
    {
      "before": ["<Leader>", "s", "j"],
      "commands": ["workbench.action.splitEditorDown"]
    },
    {
      "before": ["<Leader>", "s", "k"],
      "commands": ["workbench.action.splitEditorUp"]
    },
    {
      "before": ["<Leader>", "s", "l"],
      "commands": ["workbench.action.splitEditorRight"]
    },
    /* Git */
    {
      "before": ["<Leader>", "g", "c", "c"],
      "commands": ["git.commit"]
    },
    {
      "before": ["<Leader>", "g", "c", "a"],
      "commands": ["git.commitAll"]
    },
    {
      "before": ["<Leader>", "g", "p", "h"],
      "commands": ["git.push"]
    },
    {
      "before": ["<Leader>", "g", "p", "f"],
      "commands": ["git.pushForce"]
    },
    {
      "before": ["<Leader>", "g", "p", "l"],
      "commands": ["git.pull"]
    },
    {
      "before": ["<Leader>", "g", "c", "b"],
      "commands": ["git.branch"]
    },
    {
      "before": ["<Leader>", "g", "s", "s"],
      "commands": ["git.stash"]
    },
    {
      "before": ["<Leader>", "g", "s", "d"],
      "commands": ["git.stashDrop"]
    },
    {
      "before": ["<Leader>", "g", "s", "p"],
      "commands": ["git.stashPop"]
    },
    {
      "before": ["<Leader>", "g", "f", "f"],
      "commands": ["git.fetch"]
    },
    {
      "before": ["leader", "g", "c", "n"],
      "commands": ["workbench.action.compareEditor.nextChange"]
    },
    {
      "before": ["leader", "g", "c", "p"],
      "commands": ["workbench.action.compareEditor.previousChange"]
    },
    {
      "before": ["<Leader>", "g", "o", "c"],
      "commands": ["git.openChange"]
    },
    {
      "before": ["leader", "m", "c", "o"],
      "commands": ["merge-conflict.compare"]
    },
    {
      "before": ["leader", "m", "c", "n"],
      "commands": ["merge-conflict.next"]
    },
    {
      "before": ["leader", "m", "c", "p"],
      "commands": ["merge-conflict.previous"]
    }
  ],
  "vim.leader": ",",
  "vim.handleKeys": {
    "<C-a>": false,
    "<C-f>": false
  },
  "vim.statusBarColorControl": true,
  "vim.visualModeKeyBindingsNonRecursive": [
    {
      "before": ["<Leader>", "f"],
      "commands": ["editor.action.formatSelection"]
    }
  ],
  /* VIM Configuration end */
}
```

keybinding.json

```json
// Place your key bindings in this file to override the defaults
[
  /* splitted window focus*/
  {
    "key": "ctrl+h",
    "command": "workbench.action.focusLeftGroup",
    "when": "editorTextFocus && vim.active && vim.mode != 'Insert'"
  },
  {
    "key": "ctrl+l",
    "command": "workbench.action.focusRightGroup",
    "when": "editorTextFocus && vim.active && vim.mode != 'Insert'"
  },
  {
    "key": "ctrl+k",
    "command": "workbench.action.focusAboveGroup",
    "when": "editorTextFocus && vim.active && vim.mode != 'Insert'"
  },
  {
    "key": "ctrl+j",
    "command": "workbench.action.focusBelowGroup",
    "when": "editorTextFocus && vim.active && vim.mode != 'Insert'"
  },
  /*list move up and down*/
  {
    "key": "ctrl+k",
    "command": "list.focusUp",
    "when": "listFocus && !inputFocus"
  },
  {
    "key": "ctrl+j",
    "command": "list.focusDown",
    "when": "listFocus && !inputFocus"
  },
  {
    "key": "ctrl+j",
    "command": "selectNextSuggestion",
    "when": "suggestWidgetVisible"
  },
  {
    "key": "ctrl+k",
    "command": "selectPrevSuggestion",
    "when": "suggestWidgetVisible"
  },
  {
    "key": "ctrl+t",
    "command": "workbench.action.focusActiveEditorGroup",
    "when": "terminalFocus || filesExplorerFocus || workbench.explorer.openEditorsView.active"
  },
  {
    "key": "ctrl+t",
    "command": "workbench.action.terminal.focusNext",
    "when": "!terminalFocus && editorTextFocus && vim.active && vim.mode != 'Insert'"
  },
  /* format document */
  {
    "key": "alt+cmd+l",
    "command": "editor.action.formatDocument"
  },
  {
    "key": "cmd+e",
    "command": "workbench.files.action.showActiveFileInExplorer"
  },
  /* Explorer operation*/
  {
    "key": "a",
    "command": "explorer.newFile",
    "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceIsRoot && !inputFocus"
  },
  {
    "key": "shift+a",
    "command": "explorer.newFolder",
    "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceIsRoot && !inputFocus"
  },
  {
    "key": "y",
    "command": "filesExplorer.copy",
    "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceIsRoot && !inputFocus"
  },
  {
    "key": "x",
    "command": "filesExplorer.cut",
    "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceIsRoot && !inputFocus"
  },
  {
    "key": "p",
    "command": "filesExplorer.paste",
    "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceReadonly && !inputFocus"
  },
  {
    "key": "r",
    "command": "renameFile",
    "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
  },
  {
    "key": "d",
    "command": "moveFileToTrash",
    "when": "explorerResourceMoveableToTrash && explorerViewletVisible && filesExplorerFocus && !explorerResourceReadonly && !inputFocus"
  },
  {
    "key": "shift+d",
    "command": "deleteFile",
    "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceReadonly && !inputFocus"
  },
  {
    "key": "c",
    "command": "workbench.files.action.collapseExplorerFolders",
    "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceReadonly && !inputFocus"
  },
  {
    "key": "s",
    "command": "explorer.openToSide",
    "when": "explorerViewletFocus && explorerViewletVisible && !inputFocus"
  },
  {
    "key": "f",
    "command": "revealFileInOS",
    "when": "explorerViewletFocus && explorerViewletVisible && !inputFocus"
  },
  {
    "key": "t",
    "command": "openInTerminal",
    "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceIsRoot && !inputFocus"
  },
  {
    "key": "u",
    "command": "copyFilePath",
    "when": "explorerViewletFocus && explorerViewletVisible && !inputFocus"
  },
  {
    "key": "i",
    "command": "copyRelativeFilePath",
    "when": "explorerViewletFocus && explorerViewletVisible && !inputFocus"
  },
  /*Terminal operation */
  {
    "key": "ctrl+m",
    "command": "workbench.action.toggleMaximizedPanel",
    "when": "terminalFocus && terminalProcessSupported"
  },
  {
    "key": "ctrl+shift+j",
    "command": "workbench.action.terminal.scrollDown",
    "when": "terminalFocus && terminalProcessSupported"
  },
  {
    "key": "ctrl+shift+k",
    "command": "workbench.action.terminal.scrollUp",
    "when": "terminalFocus && terminalProcessSupported"
  },
  {
    "key": "ctrl+shift+h",
    "command": "workbench.action.terminal.scrollDownPage",
    "when": "terminalFocus && terminalProcessSupported"
  },
  {
    "key": "ctrl+shift+l",
    "command": "workbench.action.terminal.scrollUpPage",
    "when": "terminalFocus && terminalProcessSupported"
  },
  {
    "key": "ctrl+n",
    "command": "workbench.action.terminal.focusNext",
    "when": "terminalFocus && terminalProcessSupported"
  },
  {
    "key": "ctrl+shift+n",
    "command": "workbench.action.terminal.focusPrevious",
    "when": "terminalFocus && terminalProcessSupported"
  }
]

```
