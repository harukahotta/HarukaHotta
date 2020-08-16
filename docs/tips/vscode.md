---
layout: default
title: VS Code
parent: Tips
---

# VS Code
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

I know it's quite useful if I know how to use it.
There are too many functions to use it well.

## Shourtcuts for mac OS
[cheatsheet](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)

### General

|  Key  |  Operation  |
| ---- | ---- |
|  `Command + Shift + P`  |  Show Command Palette  |
|  `Command + P`  |  Quick Open, Go to File  |
|  `Control + Shift + ``  |  Open terminal |

## Extensions

### Markdown-preview-enhanced

#### import

`@import "your_file"`  

Configure images  
`@import "test.png" {width="300px" height="200px" title="my title" alt="my alt"}`

Import online file  
`@import "https://raw.githubusercontent.com/shd101wyy/markdown-preview-enhanced/master/LICENSE.md"`

Import certain lones  
`@import "test.md" {line_begin=2 line_end=10}`

Import file as Code Chunk  
`@import "test.py" {cmd="python3"}`
`@import "Hellow_World.sh" {cmd=true}`

[reference](https://shd101wyy.github.io/markdown-preview-enhanced/#/file-imports)

#### code chunk

````
```bash {cmd=true}
ls .
```
````

````
```python {cmd=true matplotlib=true}
import matplotlib.pyplot as plt
plt.plot([1,2,3, 4])
plt.show() # show figure
```
````



