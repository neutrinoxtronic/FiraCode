## Fira Code: monospaced font with programming ligatures

<img src="https://dl.dropboxusercontent.com/u/561580/imgs/fira_code_logo.svg">

### Problem

Programmers use a lot of symbols, often encoded with several characters. For the human brain, sequences like `->`, `<=` or `:=` are single logical tokens, even if they take two or three characters on the screen. Your eye spends a non-zero amount of energy to scan, parse and join multiple characters into a single logical one. Ideally, all programming languages should be designed with full-fledged Unicode symbols for operators, but that’s not the case yet.

### Solution

#### Download [Fira Code v1.102](https://github.com/tonsky/FiraCode/releases/download/1.102/FiraCode_1.102.zip) | Follow updates 📢 [@FiraCode](https://twitter.com/FiraCode)

Fira Code is an extension of the Fira Mono font containing a set of ligatures for common programming multi-character combinations. This is just a font rendering feature: underlying code remains ASCII-compatible. This helps to read and understand code faster. For some frequent sequences like `..` or `//`, ligatures allow us to correct spacing.

<img src="./showcases/all_ligatures.png" />

### Terminal support

Works | Doesn’t work
------- | ---------------
**Black Screen** | **GNOME Terminal**
**Konsole** | **iTerm 2** ([feature request](https://gitlab.com/gnachman/iterm2/issues/3568))
**QTerminal** | **rxvt**
**Terminal.app** (OS X default terminal) | **xfce4-terminal**
**Termux** (Android terminal emulator) |

### Editor support

Works | Doesn’t work
--------|----------------
**Anjuta** (ligatures rendered unless last char is at the end of file) | **Arduino IDE**
**Atom** 1.1 or newer ([instructions](https://github.com/tonsky/FiraCode/wiki/Atom-instructions)) | **Adobe Dreamweaver CS6**
**BBEdit** ([instructions](https://github.com/tonsky/FiraCode/wiki/BBEdit-instructions)) | **Eclipse** (Mac and Windows only; [vote here](https://bugs.eclipse.org/bugs/show_bug.cgi?id=398656))
**Brackets** (with [this plugin](https://github.com/polo2ro/firacode-in-brackets)) | Standalone **Emacs** ([workaround](https://github.com/tonsky/FiraCode/wiki/Setting-up-Emacs))
**Chocolat** | **gVim**
**Coda 2** | **IDLE**
**Code::Blocks IDE** | **KDevelop 4**
**CodeLite** | **Monkey Studio IDE**
**Eclipse** (Linux only) | **Netbeans**
**Geany** | **Notepad++**
**gEdit / Pluma** | **Spyder IDE**
**GNOME Builder** | **SublimeText** ([vote here](http://sublimetext.userecho.com/topic/1030059-does-sublimetext-support-programming-ligatures-fontlike-fira-code/))
**IntelliJ products** (IDEA, Android Studio, etc; [Instructions](https://github.com/tonsky/FiraCode/wiki/Intellij-products-instructions)) |
**Kate, KWrite** |
**Leafpad** |
**LibreOffice** |
**LightTable** ([instructions](https://github.com/tonsky/FiraCode/wiki/LightTable-instructions)) | 
**MacVim** 7.4 or newer ([instructions](https://github.com/tonsky/FiraCode/wiki/MacVim-instructions)) |
**Mancy** |
**Meld** |
**Mousepad** |
**Notepad** (Windows) |
**QtCreator** | 
**RStudio** ([instructions](https://github.com/tonsky/FiraCode/wiki/RStudio-instructions)) |
**Scratch** |
**TextAdept** (Linux, Mac) |
**TextEdit** (Mac OS X text editor) |
**TextMate 2** |
**Visual Studio 2015** |
**Visual Studio Code** ([instructions](https://github.com/tonsky/FiraCode/wiki/VS-Code-Instructions)) |
**Xamarin Studio/Monodevelop** |
**Xcode** (with [this plugin](https://github.com/robertvojta/LigatureXcodePlugin)) |
Probably works: **Smultron, Vico** |

### Browser support

- IE 10+ and Edge: enable with `font-feature-settings: "calt" 1;`
- Firefox
- Safari
- Chromium-based browsers (like Chrome, most Android browsers, and Opera): enable with  `font-variant-ligatures: contextual;` or `text-rendering: optimizeLegibility` (see [bug 571246](https://code.google.com/p/chromium/issues/detail?q=font-variant-ligatures&id=571246&thanks=571246&ts=1450553433&))
- ACE
- CodeMirror

### Code examples

Ruby:

<img src="./showcases/ruby.png" />

JavaScript:

<img src="./showcases/javascript.png" />

Erlang:

<img src="./showcases/erlang.png" />

Go:

<img src="./showcases/go.png" />

Haskell:

<img src="./showcases/haskell.png" />

### Alternatives

Other monospaced fonts with ligatures:

- [Hasklig](https://github.com/i-tu/Hasklig) (free)
- [PragmataPro](http://www.fsd.it/fonts/pragmatapro.htm) (€59)
- [Monoid](http://larsenwork.com/monoid/) (free)

### Credits

My name is Nikita Prokopov ([@nikitonsky](https://twitter.com/nikitonsky)).

Official Fira Code twitter: [@FiraCode](https://twitter.com/FiraCode) (subscribe for updates & announcements)

This work is based on OFL-licensed [Fira Mono font](https://github.com/mozilla/Fira). Original Fira Mono font was not changed, only extended.

Fira Code was inspired by [Hasklig font](https://github.com/i-tu/Hasklig): Ligatures for Haskell code.

Thanks Georg Seifert for providing a [Glyphs 2](https://glyphsapp.com) license.

### Changelog

#### 1.102

- Support for IntelliJ-based IDEs ([instructions](https://github.com/tonsky/FiraCode/wiki/Intellij-products-instructions))
- Turned on autohinting


#### 1.101

- Added Light weight
- Adjusted rules when vertical centering of `:`, `-`, `*` and `+` occurs


#### 1.100

- Fixed calt table conflicts (`----` would incorrectly render as `<!--`)
- Added centered `:` (between digits, e.g. `10:40`)
- Added lowercase-aligned `-`, `*` and `+` (only between lowercase letters, e.g. kebab case `var-name`, pointers `*ptr` etc)


#### 1.000

Added weights:

- Retina (just slightly heavier than Regular)
- Medium
- Bold

Switched to `calt` instead of `liga`. You can now “step inside” the ligature in text editors.

Fira Code is now drawn and built in Glyphs 2 app (should improve compatibility).

Added:

`<->` `<~~` `<~` `~~~` `~>` `~~>`  
`<$` `<+` `<*` `*>` `+>` `$>`  
`;;;` `:::` `!!!` `???` `%%` `%%%` `##` `###` `####`  
`.-` `#_(` `=<`  `**/` `0x` `www` `[]` 

Redrawn:

`{-` `-}` `~=` `=~` `=<<` `>>=` `<$>` `<=>` `.=`

Removed: `?:`

Total ligatures count: 115


#### 0.6

Redrawn from Fira Mono 3.204 (slightly heavier weight)

Added:

`**` `***` `+++` `--` `---` `?:`  
`/=` `/==` `.=` `^=` `=~` `?=` `||=` `|=`  
`<<<` `<=<` `-<<` `-<` `>-` `>>-` `>=>` `>>>`  
`<*>` `<|>` `<$>` `<+>`  
`<!--` `{-` `-}` `/**`  `\\` `\\\`
`..<` `??` `|||` `&&&` `<|` `|>`  
  
Added support for Powerline


#### 0.5

Added: `#{` `~-` `-~` `<==` `==>` `///` `;;` `</`


#### 0.4

- Added `~=` `~~` `#[`
- Rolled back `&&` and `||` to more traditional look
- `===` and `!==` are now rendered with 3 horizontal bars


#### 0.3

Added: `~@` `#?` `=:=` `=<`


#### 0.2.1

Fixed width of `&&` and `||`


#### 0.2

Added: `-->` `<--` `&&` `||` `=>>` `=/=`


#### 0.1

`>>=` `=<<` `<<=` `->>` `->` `=>` `<<-` `<-`  
`===` `==` `<=>` `>=` `<=` `>>` `<<` `!==` `!=` `<>`  
`:=` `++` `#(` `#_`  
`::` `...` `..` `!!` `//` `/*` `*/` `/>`  
