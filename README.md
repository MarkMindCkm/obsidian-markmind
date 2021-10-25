
# Obsidian mark mind

## Notice 

This is not an open source project .  
Web site : https://www.markmind.net


## Introduction

Obsidian mark mind is a mind map,outline and pdf annotate tool base on obsidian api.

## Mind map introduction

it contains  two modes : basic and rich 

Add yaml to markdown:

```yaml
---

mindmap-plugin: basic (or rich)

---
```
Then you can find `Open as mindmap` menu in `more options`

## In `basic` mode

You can  use the basic mind map function and use outline mode , it like the obsidian-enhancing-mindmap plugin.

### `basic` mode will output this mardkown:

```
---

mindmap-plugin: basic

---

# Mark mind for obsidian

## Links
- <https://github.com/MarkMindLtd/obsidian-markmind>
- [GitHub](https://github.com/MarkMindLtd/obsidian-markmind)

## Related
- [coc-markmap](https://github.com/gera2ld/coc-markmap)
- [gatsby-remark-markmap](https://github.com/gera2ld/gatsby-remark-markmap)

## Features
- links
- **inline** ~~text~~ *styles*
- multiline
   text
- `inline code`
- Katex - $x = {-b \pm \sqrt{b^2-4ac} \over 2a}$
```

### outline

You can add yaml to active outline mode:

``` 
---

mindmap-plugin: basic
display-mode: outline

---

```

#### Outline short cut

| Features             | Short Cut                       |
| -------------------- | ------------------------------- |
| New Brother Node     | Enter                           |
| Indent               | Tab                             |
| Unindent             | Shift+Tab                       |
| Zoom in              | Ctrl/Cmd+] Or Double Click Dott |
| Zoom out             | Ctrl/Cmd+[                      |
| Move Up Or Down Node | Ctrl/Cmd + up/down              |




## In `rich` mode

You can use all functions of mind map .

- add summary
- add boundary
- add node relate link
- add free node

### Rich mode will output  this  markdown:

```markdown
---

mindmap-plugin: rich

---

# md 

​``` json
{...}
​```

```

The mindmap data will store to `json`. 

### mindmap short cut

| New Mind Map                            | Ctrl/Cmd+P                   |
| --------------------------------------- | ---------------------------- |
| New child node                          | Tab                          |
| New brother node                        | enter                        |
| Delete node                             | Delete/Backspace             |
| edit node                               | Space/dblclick node          |
| Undo                                    | Ctrl/Cmd+Z                   |
| Redo                                    | Ctrl/Cmd+Y                   |
| Quit edit node                          | Tab                          |
| Expand node                             | Ctrl/Cmd + /                 |
| Collapse node                           | Ctrl/Cmd + /                 |
| Move node to another node               | Drag and drop node           |
| Tab node                                | Up/down/left/right           |
| Zoom in/out                             | Ctrl/Cmd + mouse wheel       |
| Mind map to center                      | Ctrl/Cmd + E                 |
| Change mindmap layout                   | select node,Ctrl/Cmd + U / D / L / R / M |
| delete summary / boundary / relate link | Delete/Backspace             |

---

<img src = 'https://user-images.githubusercontent.com/18719494/130028629-1a1e448d-32b9-4201-b152-1ad09439e18e.gif' width="800px">


## PDF annotate

- highlight text
- rectangular annotate
- relate  mind map node and annotate

### How to use pdf annotate
> You need download pdf js plugin ,Open setting tab  to set up pdf plugin path , for example:D:plugins/pdfjs , It is a absolute path

PC : [Pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.0/pdfjs.zip)    
Andriod [Andriod pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.0/mobile.pdfjs.zip)    
iPhone/iPad : [iPhone/iPad pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.1/ios.pdfjs.zip)  

### Markdown  
Add yaml to markdown file:  

```
---

annotate-target: test/test.pdf
annotate-type: pdf

---
```
Then you can find menu `annotate pdf` in `more options`;

### Mind Map

1. Open as mind map
2. Use `[[]]` to reference pdf
3. Click pdf reference , it will open a pdf reader if pdf plugin path is correct
4. Use pdf annotate function 
   - it will create `annos` file in your folder as default, the `annos` file store annotations data,`annos` file is a `json` file in fact
   - if you select (save pdf annotation type ) `markdown` in setting tab , it will create `${pdf name}-annotate.md` file in your folder. Each annotation has an associated quote block with a block reference. please do not  modify these blocks
   

### how to relate mind map node and annotate?

There are three ways to  relate mind map node and annotate

#### Default (only support rich mode)

- make a pdf annotate
- click pdf annotate
- edit mind map node , `ctrl/cmd + v` to relate node and annotate
- click node pdf annotate mark will auto copy `id` of annotate to clipboard


#### Support `obsidian://jump-to-pdf` protocol  (support basic and rich mode)

- open protocol support in setting tab
- automatic create PDF annotation reference link and copy to clipboard when click pdf-annotate
- paste to markdown file

#### If you use markdown to save pdf annotations  (support basic and rich mode)

-	you can use `[[${md name}#${block reference}]]` to associate quote block with a block reference.
-	An obsidian link to an annotation block-reference will, when clicked, open the corresponding file and scroll to the associated highlight. If the file is already open in a pane, then the link will cause the existing pane to scroll instead.
### Demonstration

<img src = 'https://user-images.githubusercontent.com/18719494/130031749-84b84833-a52c-4ad1-b589-00eb2d8af317.gif' width="800px">



## Donating
<a href="https://www.buymeacoffee.com/markmind"><img src="https://img.buymeacoffee.com/button-api/?text=Buy me a coffee&emoji=&slug=markmind&button_colour=FFDD00&font_colour=000000&font_family=Cookie&outline_colour=000000&coffee_colour=ffffff"></a>

## Change log  v1.1.2

fix #46  
add `set mindmap to center` menu in `more options` 

### v1.1.1
**important:**  
Mobile pdf js plugin need to download again  

PC : [Pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.0/pdfjs.zip)    
Andriod [Andriod pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.0/mobile.pdfjs.zip)    
iPhone/iPad : [iPhone/iPad pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.1/ios.pdfjs.zip)  
 

1. fix iPhone/iPad cannot use pdf annotate bug

Please set up pdfjs path in setting tab , this is a absolute path ,( you can find  absolute path of your vault in obsidian app ) the best way is create a folder in your vault , for example :`plugin` folder, then put pdfjs plugin in it 


**About iPhone/iPad pdfjs path**:
for example (iPad), you create `plugin` folder in your vault , then put `pdfjs plugin` into it , the path will like this   
`/var/mobile/Containers/Data/Application/FACF6387-DAA2-45B3-8F52-3536E1EC29A1/Documents/plugin/pdfjs`  

`FACF6387-DAA2-45B3-8F52-3536E1EC29A1`  are different on each device  

**About andriod pdfjs path**,like this  
`/storage/emulated/0/Documents/obsidian/obsidian/plugin/pdfjs`  

**About PC pdfjs path**,like this  

`D:plugin/pdfjs`

---

iPad screen short
![68747470733a2f2f692e6c6f6c692e6e65742f323032312f31302f31312f3431557933536d756a4b723835515a2e706e67](https://user-images.githubusercontent.com/18719494/136878933-3c86d930-e2fd-4dd4-8c1e-8c4de6cc1ac7.png)


### v1.1.0
**Important**
In this version ,You should download pdfjs plugin again

PC : [Pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.0/pdfjs.zip)    
Andriod [Andriod pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.0/mobile.pdfjs.zip)    
iPhone/iPad : [iPhone/iPad pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.1/ios.pdfjs.zip)  

You should set up pdf js plugin path in setting tab , it is a absolute path   
**For example** : 
  - ` D:plugins/pdfjs `   in pc 
  - `/storage/emulated/0/Documents/obsidian/obsidian/plugin/pdfjs`  in andriod

you should put pdfjs plugin to a accessible folder in mobile . 
you can find your vault  path in mobile app , the best way is create a folder(for example `plugin` folder) in your vault  , then put pdfjs plugin in it.


1. fix #40  ， you can select mode  of mindmap  (when create mindmap) in setting tab , the default is `basic`
2. pdf annotate support mobile , only support pdf of your vault , not support `file://`
3. in md file , support use `[[md#^node id]]`  to reference  node of `rich` mode mindmap , you can find menu `copy node id` in `more options`
4. support set up image folder in setting tab to save image of pdf rect annotate .
   - for example :  `Screenshot` , the Screenshot folder must be exists  in your vault, the image of rect annotate will be save to `Screenshot` folder
   
5. fix when annotate `file:// pdf path` cannot use rect annotate bug
6. support 3 theme of mindmap , you can add yaml to markdown
``` 
---

mindmap-plugin: basic( or rich )
mindmap-theme: dark(or light or card)  

---
```

Markmind all functions will support mobile and pc from this version ,andriod/apple/window/linux has consistent experience.


<img src="https://user-images.githubusercontent.com/18719494/136696974-a776ad2c-aab5-4d62-917f-2b294d1da40a.gif" width="300"/> <img src="https://user-images.githubusercontent.com/18719494/136696996-36cd0e77-8212-4b6f-8f55-6dbf617cf906.gif" width="300"/>

![动画1211713467](https://user-images.githubusercontent.com/18719494/136694951-9bb9720d-b5e3-4622-8929-70de6fb7f24a.gif)

## v1.0.9
### this is a big version

1. fix #4 ,  pdf annotate support all pdf files on disks by using `file://` ，this feature can only use to  desktop app  , if you use `file://` , the annotatios will be save to this markdown file 

```
annotate-target: file://pdf absolute path
annotate-type: pdf

```
2. fix #29 , support mobile from this version， it has consistent experience with desktop version

3. add command :
- select node , change layout  in `rich` mode of mindmap
- toggle markdown and mindmap mode
- add some menus of `more options` in `rich` mode of mindmap ，(copy text to clipboard automatic)
   - Copy node text  as markdown (contains children)，the text type like `basic` mode
   - Copy node text (only this node)
   - Copy node links , you can reference it in other md file
 
4. support change summary/boundary/relate link color
5. if you set up active code in setting tab of desktop version , it will create mobile active code in your plugin obsidian-markmind data.json automatic
6. support move root of mindmap in rich mode

![12117](https://user-images.githubusercontent.com/18719494/135819440-34380383-0a3a-481c-b5ac-205f6a9da155.gif)
<img src="https://user-images.githubusercontent.com/18719494/135823093-f34d6870-7dfb-4646-8874-1347ad5047f0.gif" width="300"/>


### v1.0.8

fix #26  
fix miss markdown format in `list` mode when use ctrl + down / up

### v1.0.7
fix #24 , fix pdf select multi line to highlight , this problem is caused by pdf plugin  

 **Important**:
 **You should to download the pdfjs plugin again PDFJS Plugin, it keep more functions and it support multi open**  
PC : [Pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.0/pdfjs.zip)    
Andriod [Andriod pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.0/mobile.pdfjs.zip)    
iPhone/iPad : [iPhone/iPad pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.1/ios.pdfjs.zip)  

### v1.0.6
emergency fix #22  
emergency fix #21

### v1.0.5  

emergency fix mindmap `rich` mode bug

### v1.0.4


This is a big version: 
 **Notice**:
 **You should to download the pdfjs plugin  [PDFJS Plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.0.7/pdfjs.zip), it keep more functions and it support multi open**

1, fix #18 , you can select pdf viewer theme in setting tab  
2. fix #17   
3. fix #15   
4. fix #8   
5. Support multi open pdf annotate  
6. support add comment to annotation  
7. support committing highlights and notes to PDFs ，you can find `export pdf annotate` menu in more menus , it will create a file in your folder,the name is `${pdf name}-annotate.pdf`  
8. Split PDF annotation and mindmap function  
9. change in  `basic` mode , mind map layout from `tree` to `mind map`   
10. fix #2 , in `rich` mode  
 - if save data first time , it will output this markdown   
 - if it is not the first time to save data , it will only replace '${mindmap data}', so you can change `md` file  
 - if you want to reference node ,  it will automatic create mind map node reference link and copy to clipboard when click node and press ctrl or command  
<pre>  
---
mindmap-plugin: rich
---

# title
``` json
  ${mindmap data}
```

</pre>  
 
<hr>  
  
The use type of PDF annotation has changed , if you want to use annotate function, you can add `yaml` to markdown file:  

```
---

annotate-target: test/test.pdf
annotate-type: pdf

---
```

then you can find `annotate pdf` menu in more menus  

1. you can select `md` or `annos` to save annotations in setting tab  
  - `annos` is default , it is `json` file in fact , you can use `obsidian://jump-to-pdf` to reference annotate ,  
      - annotations do not contaminate MD files When referenced  
  - `md` is the recommended way   
     - you can use `obsidian://jump-to-pdf` to reference annotate 
     -  or you can ![[ md#^block id]] to to reference annotate  
 2. please open `obsidian://jump-to-pdf` protocol in setting tab  
 
<hr>  
<br>
<br>


