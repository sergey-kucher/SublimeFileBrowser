# FileBrowser for SublimeText
Ditch sidebar and browse your files in a normal tab with keyboard, like a pro!

![SublimeFileBrowser Screenshot](http://cl.ly/image/152u1c3J3U45/Screen%20Shot%202014-01-24%20at%2011.30.34.png)

You can also use it as a sidebar that you can put on right or left side
![SublimeFileBrowser Screenshot2](http://cl.ly/image/0Z2U062k3l3p/Screen%20Shot%202014-01-24%20at%2011.26.53.png)

## Installation
You can install via [Sublime Package Control](http://wbond.net/sublime_packages/package_control)  
Or you can clone this repo into your Sublime Text Packages folder and rename the folder to `FileBrowser`

## Commands and Keybindings
This plugin does not add any keybindings for opening a new tab in "Browse mode". Although, the commands to do that are available in *command pallete* but I recommend binding <kbd>F1</kbd> to open the current file folder in "Browse mode" with this peice of code (that you can add it to your `Key Bindings - User` file):

``` json
{ 
  "keys": ["f1"], 
  "command": "dired", 
  "args": { "immediate": true } 
}
```


| Commands                                 | Description                                       |
| :--------------------------------------- | :------------------------------------------------ |
| **Browse Mode...**                       | Asks for a directory to open in browse mode       |
| **Browse Mode: Current file or project** | Open the directory of current file in browse mode |

### Shortcuts

| Command                       | Shortcut                               |
| :-----------------------------| :--------------------------------------|
| Help page                     | <kbd>?</kbd>                           |
| Toggle mark                   | <kbd>m</kbd>                           |
| Toggle mark and move down     | <kbd>shift+↓</kbd>                     |
| Toggle mark and move up       | <kbd>shift+↑</kbd>                     |
| Toggle all marks              | <kbd>t</kbd>                           |
| Unmark all                    | <kbd>u</kbd>                           |
| Mark by extension             | <kbd>\*</kbd>                          |
| Rename                        | <kbd>R</kbd>                           |
| Move                          | <kbd>M</kbd>                           |
| Delete                        | <kbd>D</kbd>                           |
| Send to trash                 | <kbd>S</kbd>                           |
| Create directory              | <kbd>cd</kbd>                          |
| Create file                   | <kbd>cf</kbd>                          |
| Open file/view directory      | <kbd>o</kbd>                           |
| Open file in another group    | <kbd>enter</kbd>                       |
| Preview file in another group | <kbd>shift+enter</kbd>                 |
| Open in Finder/File Explorer  | <kbd>\\</kbd>                          |
| Open in new window            | <kbd>w</kbd>                           |
| Go to parent directory        | <kbd>backspace</kbd>                   |
| Go to directory               | <kbd>g</kbd>                           |
| Quick jump to directory       | <kbd>p</kbd>                           |
| Create/Edit/Remove jump point | <kbd>P</kbd>                           |
| Go to first                   | <kbd>⌘+↑</kbd> or <kbd>ctrl+home</kbd> |
| Go to last                    | <kbd>⌘+↓</kbd> or <kbd>ctrl+end</kbd>  |
| Move to previous              | <kbd>k</kbd> or <kbd>↑</kbd>           |
| Move to next                  | <kbd>j</kbd> or <kbd>↓</kbd>           |
| Jump to                       | <kbd>/</kbd>                           |
| Refresh view                  | <kbd>r</kbd>                           |
| Toggle hidden files           | <kbd>h</kbd>                           |
| Toggle add folder to project  | <kbd>f</kbd>                           |
| Set current folder as         | <kbd>F</kbd>                           |
| only one for the project      |                                        |
| Quicklook for Mac             | <kbd>space</kbd>                       |

In **Rename Mode**:

| Command          | Shortcut               |
| :--------------- | :--------------------- |
| Apply changes    | <kbd>enter</kbd>       |
| Discard changes  | <kbd>escape</kbd>      |


### Selecting Files and Directories
You can select files and/or directories by marking them with <kbd>m</kbd>, or <kbd>Shift+up/down</kbd> or just use the sublime multiple cursor feature and extend your cursor to the line that has those files/directories

### Rename Mode
The rename command puts the view into **rename mode**. The view is made editable so files can be renamed directly in the view using all of your Sublime Text tools: multiple cursors, search and replace, etc.

After you are done with editing press <kbd>super+enter</kbd> to commit your changes or <kbd>escape</kbd> to cancel them.

### Open in new window
Selecting a couple of files and/or directories (either by marking them or using the noraml multiple cursor feature of sublime) and pressing <kbd>w</kbd> will open them in a new SublimeText window. 

### Customizing UI
If you don't like `⠤` symbol and want to hide it (then you should use keyboard binding `backspace` to go to parent directory) you can do it in your user syntax specific settings file. create a file called `dired.sublime-settings` in you User folder and paste the code below:

``` json
{
  "dired_show_parent": false,
}
```

## Changing color scheme
If you don't like colors used in FileBrowser just copy [this file](https://github.com/aziz/SublimeFileBrowser/blob/master/dired.hidden-tmTheme) to your User folder, change colors and create a file called `dired.sublime-settings` in you User folder and paste the code below:

``` json
{
  "color_scheme": "Path to your custom color scheme file. e.g. Packages/User/custom_dired.hidden-tmTheme",
}
```

## Credit
This is a fork of the awesome [dired plugin](https://github.com/mkleehammer/dired) by [Michael Kleehammer](https://github.com/mkleehammer)

#### License
See the LICENSE file
