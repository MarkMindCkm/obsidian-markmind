
# Obsidian mark mind

[中文手册](https://github.com/MarkMindCkm/obsidian-markmind/blob/main/docs/%E7%94%A8%E6%88%B7%E6%89%8B%E5%86%8C.md)

## Notice 

This is not an open source project .  
Web site : https://www.markmind.net

### Price

| free  | Catalyst |
| -------------------- | ------------------------------- |
|  `basic` mode of mindmap |  advanced features in  `rich` mode of mind map       |
|  most features in `rich` mode of mindmap                                     |   pdf annotate                    |
|    list mode         |        support development                                            |
|    support mobile and pc         |       support mobile and pc                                           |
|    $0         |      $12 （forever）                                          |
|           |       [Buy](https://www.markmind.net)                                        |


You can try it for 30 days for free，and you can buy a active code in website , then input it in setting tab 


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

### `basic` mode will output this markdown:

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

### Outline

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


![outline](https://user-images.githubusercontent.com/18719494/138630597-fc2396d1-c818-43dc-83eb-fa638d8a0028.gif)



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
| Change mindmap layout                   | select node,Ctrl/Cmd + U / D / L / R / M / J |
| delete summary / boundary / relate link | Delete/Backspace             |

---

<img src = 'https://user-images.githubusercontent.com/18719494/130028629-1a1e448d-32b9-4201-b152-1ad09439e18e.gif' width="800px">

#### How to get markdown in `rich` mode ?
You can find `Copy as markdown` menu in `more options`.

<img src = 'https://user-images.githubusercontent.com/18719494/142220099-a69fa850-4ead-465a-98e5-f45611b48b55.gif' width='800px'>



## PDF annotate

- highlight text
- rectangular annotate
- relate  mind map node and annotate

### How to use pdf annotate
> You need download pdf js plugin ,Open setting tab  to set up pdf plugin path , for example:D:plugins/pdfjs , It is a absolute path

[PC pdfjs plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.2.0/pdfjs.zip)   
[andrios pdfjs plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.2.0/andriod.pdfjs.zip)   
[ios pdfjs plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.2.0/ios.pdfjs.zip)   


**About iPhone/iPad pdfjs path**:
for example (iPad), you create `ios` folder in your vault , then put `pdfjs plugin` into it , the path will like this 
`/var/mobile/Containers/Data/Application/FACF6387-DAA2-45B3-8F52-3536E1EC29A1/Documents/ios/pdfjs`

`FACF6387-DAA2-45B3-8F52-3536E1EC29A1`  are different on each device 

**About andriod pdfjs path**,for example,like this
`/storage/emulated/0/Documents/obsidian/obsidian/andriod/pdfjs`

**About PC pdfjs path**,like this

`D:plugin/pdfjs`


#### How to set up your pdfjs plugin path?
In pc , you can open setting tab and input  absolute path to  `pdfjs plugin`   
In mobile , you can open command board , then you can find a `set up mobile pdf js plugin path` command ,then click it   

- download lastest pdfjs plugin ，unzip it  
- in andriod , create a `andriod` folder then put `pdfjs` folder in it  
- in ios , create a `ios` folder then put `pdfjs` folder in it  
- open a mind map  
- call up command board , then you can find a set up mobile pdfjs plugin path command , click it  
- restart obsidian and check path in obsidian markmind setting tab    

The pdf js path need set separately and if it is not work above in ios , you can try `filza` app , it can find obsidian path


### Markdown  
Add yaml to markdown file:  

```
---

annotate-target: test/test.pdf
annotate-type: pdf

---
```
Then you can find menu `annotate pdf` in `more options`;

### short cut of pdf annoate

| Features             | Short Cut                       |
| -------------------- | ------------------------------- |
|  Highlight Yellow    | ALT + Y                          |
| Highlight Green                | ALT + G                            |
|  Highlight Blue             | ALT + B                       |
|  Highlight Pink         | ALT + P |
| Highlight Red            |ALT + R                     |
|Delete annotate  |    ALT + Delete/Backspace             |

### Mind Map and pdf annotate 

1. Open as mind map
2. Use `[[]]` to reference pdf
3. Click pdf reference , it will open a pdf reader if pdf plugin path is correct
4. Use pdf annotate function 
   - it will create `annos` file in your folder as default, the `annos` file store annotations data,`annos` file is a `json` file in fact
   - if you select (save pdf annotation type ) `markdown` in setting tab , it will create `${pdf name}-annotate.md` file in your folder. Each annotation has an associated quote block with a block reference. please do not  modify these blocks
   

### How to relate mind map node and annotate?

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

## Change log  v1.2.6

1. add more options of canvas size in setting tab
2. optimize the logic of the pop-up node setting box
3. support export mindmap to html , use ctrl + p , then you can find export to html command , notice :
  - not support blank link
  - not suport ![[svg/pdf/mp4]] , only support ![[png/jpg]] in node , image in mindmap must be local
  - support export mathematical formul
  - not support mobile
  
---  

![1234](https://user-images.githubusercontent.com/18719494/147195606-3a270e5e-2628-4322-bd87-9ef6d1004b66.gif)


### 1.2.5

- Optimize the interaction of node setting box
- ctrl/cmd + mouse click to select nodes , not support right click
- add set up mac pdf js plugin path
- notice : enhancing mindmap support export mindmap to image , it will be transplanted soon

### 1.2.4

- Right click to select nodes and left click to move the mind map  
- In rich mode , support set up node background/stroke/text color/text size，if you want to change colors of node setup board , you can input setup board color in setting tab please restart obsidian


### 1.2.3
fix v1.2.2 tab/enter bug

### v1.2.2

1. fix #108
2. fix #103
3. add `copy and paste` command (ctrl + p ) , support copy and paste node on mind maps
4. Optimize input, select the node, press spacebar to edit the node in append mode, and press other keys to edit in overwrite mode


### v1.2.1

**Nitice:**   
Please update pdfjs plugin to v1.2.0 , the pc support epub file , the detail is there [v1.2.0](https://github.com/MarkMindCkm/obsidian-markmind/releases/tag/1.2.0)  

fix set up pdf js plugin bug  

***How to set up pdf js plugin ***
- download lastest pdfjs plugin ，unzip it  
- in andriod , create a `andriod` folder then put `pdfjs` folder in it  
- in ios , create a `ios` folder then put `pdfjs` folder in it  
- open a mind map  
- call up command board , then you can find a set up mobile pdfjs plugin path command , click it  
- restart obsidian and check path in obsidian markmind setting tab    
 

The pdf js path need set separately and if it is not work above in ios , you can try `filza` app , it can find obsidian path


### v1.2.0


**Important**  
Please update pdfjs plugin ,  pc version  support epub file , mobile will support near future    
[PC pdfjs plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.2.0/pdfjs.zip)   
[andrios pdfjs plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.2.0/andriod.pdfjs.zip)   
[ios pdfjs plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.2.0/ios.pdfjs.zip)   

----


1. fix #87 
2. support read and annotate epub file,this is beta function

 add yaml to md 

<pre>

---

annotate-target: test.epub
annotate-type: epub

---

</pre>


then you can find `annotate epub` in `more options`


3. fix miss `$` when save data bug
4. simplify set up mobile pdfjs plugin path

      - download lastest pdfjs plugin ，unzip it
      - in andriod , create a `andriod` folder then put `pdfjs` folder in it 
      - in ios , create a `ios` folder then put `pdfjs` folder in it 
      - open a mind map
      - call up command board , then you can find a `set up mobile pdfjs plugin path` command , click it
  


----
### epub  
![test1](https://user-images.githubusercontent.com/18719494/144242980-afc1100c-c31e-4d80-9cc8-6eb46387ec6c.gif)

### set up mobile pdf js plugin path

https://user-images.githubusercontent.com/18719494/144244497-4dd9e79c-3b50-4974-81c8-ea1a7ef92310.mp4



### v1.1.9

**Important :  ios pdfjs plugin update !**

1. fix cannot use highlight text in ios system [ download ios pdfjs plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.9/ios.pdfjs.zip)
2. support parse code block in markdown file , you should open it in setting tab and restart obsidian
<pre>

``` mindmap

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
</pre>

---

![1234](https://user-images.githubusercontent.com/18719494/142712174-9ee6abc8-7aed-4159-940d-3dae6561e559.gif)

#### ipad annotate

https://user-images.githubusercontent.com/18719494/142714629-29808aa0-4d5d-46c8-8bd4-037c28dc33ae.mp4

### v1.1.8

**important**:  please update pc pdf js  to v1.1.7

[pc pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.7/pdfjs.zip)


1. support a new layout in `rich` mode of mind map , the short cut is `Ctrl/Cmd + J`
2. support import xmind zen file in `rich` mode of mind map ,  the way is  drag xmind zen file and drop to blank space of mind map in `rich` mode
3. fix some times can not add/remove free node bug

This is a xmind zen [demo](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.8/note.taking.1.xmind)    

----
Import xmind zen file  
![note 12367133](https://user-images.githubusercontent.com/18719494/141953779-f7e1fdf2-8e0f-4ab0-b099-7d5bfb7a07f5.gif)  

`Ctrl + J` change to new layout  
![note 12367133tt](https://user-images.githubusercontent.com/18719494/141953811-9657cf8d-e04e-4c7b-8499-154f9e3272d5.gif)


### v1.1.7  
**important**:  please update pc pdf js 

[pc pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.7/pdfjs.zip)  

1.  fix `basic` mode can add free node bug  
2.  fix export annotate pdf in pc version  

### v1.1.6
**important**
> please update pc pdfjs plugin  ， mobile pdfjs plugin will update next version

[PC pdfjs plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.6/pdfjs.zip)

1. fix #60 ,  add pdf annotate short cut
2. fix #61
3. fix #64 
4. fix #66 
5. mindmap node  support  smooth  move , you shoud open it in setting tab
6. In rich mode of mindmap , double click the blank space can add free node
7. fix #57

|pdf annotate Features             | Short Cut                       |
| -------------------- | ------------------------------- |
|  Highlight Yellow    | ALT + Y                          |
| Highlight Green                | ALT + G                            |
|  Highlight Blue             | ALT + B                       |
|  Highlight Pink         | ALT + P |
| Highlight Red            |ALT + R                     |
|Delete annotate  |    ALT + Delete/Backspace             |

![note 1236](https://user-images.githubusercontent.com/18719494/140644085-fc8c9f2e-d058-4ff5-a436-7edd58e33b42.gif)  



### v1.1.5
**important:**  
Please update pdfjs plugin to v1.1.1 version

PC  : [PC pdfjs plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.6/pdfjs.zip)  
Andriod [Andriod pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.0/mobile.pdfjs.zip)    
iPhone/iPad : [iPhone/iPad pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.9/ios.pdfjs.zip)  

1.  support add note to mind map node in rich mode , note support markdown  
2. summary node support add child node  
3.  (ctrl + p) add a command `get base path of vault`  , it will auto copy to clipboard  

---

![note](https://user-images.githubusercontent.com/18719494/139576838-812bf0c5-84e5-452e-accb-738517ebe7a9.gif)  

![123421](https://user-images.githubusercontent.com/18719494/139576842-3a2293a5-8238-4eb6-8475-1071ee5f14f5.gif)  


### v1.1.4
fix delete summary bug when edit node use backspace/delete key

### v1.1.3
fix #54   
fix #28  
fix miss code and link bug in outline mode  

### v1.1.2
fix #46  
add `set mindmap to center` menu in `more options` 

### v1.1.1
**important:**  
Mobile pdf js plugin need to download again  

PC:  [PC pdfjs plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.6/pdfjs.zip)    
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

PC : [Pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.7/pdfjs.zip)    
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
PC : [Pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/1.1.7/pdfjs.zip)    
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


