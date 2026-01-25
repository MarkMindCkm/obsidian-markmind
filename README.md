# Obsidian MarkMind

[中文手册](https://github.com/MarkMindCkm/obsidian-MarkMind/blob/main/docs/%E7%94%A8%E6%88%B7%E6%89%8B%E5%86%8C.md)

### **Notice**

This is not an open source project but [lishid](https://github.com/lishid) (obsidian developer) can check this code

### Feature Comparison

| Free                                     | Catalyst                                           |
| ---------------------------------------- | -------------------------------------------------- |
|  `Basic` mode of MindMap                 | Advanced features in `Rich` mode of MindMap        |
|  Most features in `Rich` mode of MindMap | PDF annotate                                       |
|  List mode                               | Support development                                |
|  PC and Mobile support                   | PC and Mobile support                              |
|  Not support                             | Export mindmap as pdf file                         |
|  $0                                      | $16 (forever) Buy [here](https://www.MarkMind.net) |

You can try it for 30 days for free. After 30 days, you can purchase a code on the website

## MarkMind docs navigation

## Vedio

- [How to use basic mode of MindMap](https://www.youtube.com/watch?v=7SkIHeQOI44)
- [How to use markdown mode of MindMap](https://www.youtube.com/watch?v=87dnyg4vEBo)
- [How to use rich mode of MindMap](https://www.youtube.com/watch?v=d65gWBZOJKQ)


### MarkMind
- [Create basic mode of MindMap](https://markmindckm.github.io/markmind-docs/index.html#/basic)
- [Display basic mode to outline](https://markmindckm.github.io/markmind-docs/index.html#/outline)
- [Display basic mode to table](https://markmindckm.github.io/markmind-docs/index.html#/table)
- [Create rich mode of MindMap](https://markmindckm.github.io/markmind-docs/index.html#/rich) ----- [youtube vedio](https://www.youtube.com/watch?v=d65gWBZOJKQ)
- [Get markdown text from rich mode of MindMap](https://markmindckm.github.io/markmind-docs/index.html#/markdown)
- [Copy and paste node of MindMap](https://markmindckm.github.io/markmind-docs/index.html#/copy)
- [Embed MindMap in other markdown file](https://markmindckm.github.io/markmind-docs/index.html#/embed)
- [Common operations of MindMap](https://markmindckm.github.io/markmind-docs/index.html#/common)
   - Drag image from desktop to rich mode of MindMap
   - Copy text from browser to MindMap
   - Drag multiple nodes

### PDF annotation

- [PDF annotate](https://github.com/MarkMindCkm/obsidian-markmind/blob/main/README.md#pdf-annotate)
- youtube: https://www.youtube.com/watch?v=07leD_6CE5E


## Introduction

Obsidian MarkMind is a mind map, outline, and PDF annotate tool based on Obsidian API

### Features:

- Links
- **Inline** ~~text~~ *styles*
- <p> Multiline<br>
   text</p>
- `inline code`
- Katex - $x = {-b \pm \sqrt{b^2-4ac} \over 2a}$

### Links:

- GitHub: https://github.com/MarkMindCkm/obsidian-MarkMind
- Changelog: [Here](/Changelog.md)
- Web site: https://www.MarkMind.net
- Join our Discord: https://discord.gg/8653ZWX649
- Chinese Readme: [中文手册](https://github.com/MarkMindCkm/obsidian-MarkMind/blob/main/docs/%E7%94%A8%E6%88%B7%E6%89%8B%E5%86%8C.md)

### Related:

- [coc-markmap](https://github.com/gera2ld/coc-markmap)
- [gatsby-remark-markmap](https://github.com/gera2ld/gatsby-remark-markmap)

## Creating a MindMap file

- It contains two modes: `Basic` and `Rich`
- You can create a MindMap file by either:
   - Right clicking a folder and selecting `New MindMap Board`
   - Add the YAML code by hand:

```YAML
---

mindmap-plugin: basic (or rich)

---
```

## Modes

### Basic

You can use the basic mind map function in conjunction with the outline or table mode. It works similar to the obsidian-enhancing-MindMap plugin. All of these modes are available in rich mode as well

#### Outline

To access the Outline mode you can either:

- Click `More options` on the note and then `Open outline`
- Add the YAML code by hand:

```YAML
---

mindmap-plugin: basic
display-mode: outline

---
```

##### MindMap Outline short cuts

| Feature                               | Short Cut                                 |
| ------------------------------------- | ----------------------------------------- |
| New Mind Map                          | CTRL/CMD + P                              |
| New Child Node                        | Enter                                     |
| Indent                                | Tab                                       |
| Unindent                              | Shift + Tab                                |
| Zoom in                               | CTRL/CMD + ] or Double click bullet point |
| Zoom out                              | CTRL/CMD + [                              |
| Zoom in/out                           | CTRL + Mouse wheel                        |
| Mind map to center                    | CTRL/CMD + E                              |
| Move Up Or Down Node                  | CTRL/CMD + Up/Down                        |
| Delete node                           | Delete/Backspace                          |
| Edit node                             | Space/Double click node                   |
| Undo                                  | CTRL/CMD + Z                              |
| Redo                                  | CTRL/CMD + Y                              |
| Expand/Collapse node                  | CTRL/CMD + /                              |
| Move node to another node             | Drag and drop node                        |
| Tab node                              | Up/Down/Left/Right                        |
| Change MindMap layout                 | Select node, CTRL/CMD + U/D/L/R/M/J/K/T/Q |
| Delete summary/boundary/related link  | Delete/Backspace                          |

![outline](https://user-images.githubusercontent.com/18719494/138630597-fc2396d1-c818-43dc-83eb-fa638d8a0028.gif)

#### Table

To access the Table mode you can either:

- Click `More options` on the note and then `Open as table`
- Add the YAML code by hand:

```YAML
---

mindmap-plugin: basic
display-mode: table

---
```

![table](https://user-images.githubusercontent.com/18719494/150626028-8d8733d5-8cd2-4eaf-b369-73ebbbcc5244.gif)

### Rich

In Rich mode you can use all the functions of basic mode. In addition you can:

- Add a summary
- Add a boundary
- Add a node related link
- Add a free node

#### Rich mode markdown format:

```YAML
---

mindmap-plugin: rich

---

# md 

{JSON Data}
```

<img src = 'https://user-images.githubusercontent.com/18719494/130028629-1a1e448d-32b9-4201-b152-1ad09439e18e.gif' width="800px">

### Other functions

- Exporting MindMap to image
   - Use `CTRL + P` and click `Export to HTML` command
- Getting markdown in `rich` mode
   - You can find `Copy as markdown` menu in `More options`
- Exporting MindMap to pdf
   - download lasted obsidian,open a mind map in a independ window
   - Use `CTRL + P` and click `Export mindmap as a pdf file` command

<img src = 'https://user-images.githubusercontent.com/18719494/142220099-a69fa850-4ead-465a-98e5-f45611b48b55.gif' width='800px'>




----

## Notice
At present, pdf annotation only supports obsidian 1.4 version ([issue](https://github.com/obsidianmd/obsidian-api/issues/142)). If you use obsidian 1.5 or later, please use markmind software([Download](https://github.com/MarkMindCkm/MarkMind-ltd/releases)) version, which can be used with obsidian and is compatible with this plug-in.

----


## PDF annotate 
- use PDF++ plugin
- highlight annotate
- rect annotate
- Relate MindMap node and annotate

### How to use PDF annotate
- download PDF++ plugin 
- if open annotate support in markmind setting tab , please close it
<img width="300" height="80" alt="QQ_1753756220445" src="https://github.com/user-attachments/assets/917fd382-fa4f-4e40-a01d-011de697c164" />

- open a pdf
- make a hihlight or rect annotate
- paste (ctrl v) in a node of mindmap

#### annotate vedio


https://github.com/user-attachments/assets/464a8db5-7d47-4dae-9a74-96107687525e


https://github.com/user-attachments/assets/8436d83e-3dae-4745-b478-71ffa6822ca1




<!--

## PDF annotate 

- Highlight text
- Area annotate
- Relate MindMap node and annotate

### How to use PDF annotate

1. Download the appropriate [PDFJS plugins](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.8.2/pdfjs.zip)
2. Install PDFJS plugin:
   - On Android, create an `andriod` folder then extract `pdfjs` folder into it
   - On IOS, create an `ios` folder, then extract `pdfjs` folder into it
      - The PDFJS path is set separately and if it does not you can try `filza` app, it can find the path to Obsidian
   - On PC, extract `pdfjs` folder to `.obsidian` folder
      - `CTRL/CMD + P`, click `set up pdfjs plugin path`
   - On Mac `Command + Shift+ .` to show the hidden folder, extract `pdfjs` folder to `.obsidian` folder
   - Restart Obsidian
3. Ensure these folders are present in PDFJS folder (VaultLocation\.obsidian\pdfjs):
   - build
   - epub
   - epub.js
   - pdfextrct
   - web
4. Add the following YAML code to the MindMap document:

```YAML
---

annotate-target: test/test.PDF
annotate-type: pdf

---
```

5. Then you can find `Annotate PDF` in `more options`

### Screenshot folder for rect annotations

1. In the MindMap plugin settings you can set a folder path
   - This should be a relative path pointing to your vault folder
2. Or you can add the folder path in YAML:

```YAML
---

annotate-target: test/test.PDF
annotate-type: pdf
annotate-image-target: assets/image

---
```

### Short Cuts for annotate

| Feature            | Short Cut                       |
| ------------------ | ------------------------------- |
| Highlight Yellow   | CTRL/CMD/ALT + Y                |
| Highlight Green    | CTRL/CMD/ALT + G                |
| Highlight Blue     | CTRL/CMD/ALT + B                |
| Highlight Pink     | CTRL/CMD/ALT + P                |
| Highlight Red      | CTRL/CMD/ALT + R                |
| Delete annotate    | CTRL/CMD/ALT + Delete/Backspace |

### Mind Map and PDF annotate

1. Open file as MindMap
2. Use `[[]]` to reference PDF
3. Click PDF reference, it will open a PDF reader if the PDF plugin path is correct
4. Use the PDF annotate function:
   - It will create an `annos` file in your current folder by default, the `annos`
   - The `annos` file stores annotations data in JSON format
   - If you set the `Save PDF annotation type` as `markdown` in setting tab, it will create a `${PDF name}-annotate.md` file in your current folder
   - Each annotation has an associated quote block with a block reference
      - **Please do not modify these blocks**

### Relating MindMap nodes and annotations

There are three ways to relate mind map node and annotations

1. Default (Only supports rich mode)
   - Make a PDF annotation
   - Click PDF annotate
   - Edit MindMap node and hit `CTRL/CMD + V` to relate the node and annotations
   - Click the node PDF annotation and it will will auto copy the `id` of the annotation to your clipboard
2. Jumpto protocol `obsidian://jump-to-PDF` (Supports basic and rich mode)
   - In MindMark settings, set `Support protocol` to `Open`
   - This will automatically create a PDF annotation reference link and copy to your clipboard when you click PDF-annotate
   - Paste into markdown file
3. Use markdown to save PDF annotations (Supports basic and rich mode)
   - You can use `[[${md name}#${block reference}]]` to associate a quote block with a block reference
   - An obsidian link to an annotation block-reference will, when clicked, open the corresponding file and scroll to the associated highlight
   - If the file is already open in a pane, then the link will cause the existing pane to scroll instead

### Importing PDF highlight annotations

1. You can use `CTRL + P` and then the change basic to rich mode command
2. Import highlight annotations from PDF 
   - You can find this in the `more options` menu when opening a PDF
3. You can also export PDF annotations in the PDF format
   - In the `more options` menu for the MindMap document
   - You can set the format you want in the MarkMind settings tab
   - The default format is:
```
Page:{{page}}
Text:{{highlightText}}
Comment:{{comment}}
^{{id}}
```

#### Demonstration

<img src = 'https://user-images.githubusercontent.com/18719494/130031749-84b84833-a52c-4ad1-b589-00eb2d8af317.gif' width="800px">

-->

## Donating

<a href="https://www.buymeacoffee.com/markmind"><img src="https://img.buymeacoffee.com/button-api/?text=Buy me a coffee&emoji=&slug=markmind&button_colour=FFDD00&font_colour=000000&font_family=Cookie&outline_colour=000000&coffee_colour=ffffff"></a>

---

### ChangeLog

#### v1.7.2

> This is a major version update !

[Download PDFjs plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.7.2/pdfjs.zip)

1. add a table layout for rich mindmap
2. update `andoird` and `ios` pdfjs plugin , the version will be same as pc version
3. fix `only copy annotate link` in setting tab of markmind , now the link type is `[📌](link)`
4. fix the image name of rect annotate,not paste path in `[[  ]]`
5. Open mind map increases speed

The program is becoming increasingly complex and difficult, please support me！

[Buy a active code](https://www.markmind.net)

The prices will be adjusted soon


---
这是一次大的版本更新，请注意！
[下载 PDFjs 插件](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.7.2/pdfjs.zip)

1.  增加表格布局
2. 更新安卓和 ios 的 pdfjs 和电脑版本一致，现在可以在不同系统之间通用
3. 修复 只复制标注链接 的 问题
4. 修复复制矩形标注的链接，去掉其中的图片路径，只使用图片名称
5. 增加打开思维导图的速度

程序越来越复杂，难度越来越大，请支持我!
[购买一个激活码](https://www.markmind.net/cn)

也许后面会调整价格。

----


![table](https://github.com/MarkMindCkm/obsidian-markmind/assets/18719494/70c90efb-3b15-4216-8c9b-874b5cf87b5e)

