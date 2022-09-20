# Changelog

## v1.5.7

1. Fix #326 
   - Support import image from xmind zen file when dragging xmind zen file to `rich` mode
   - You must set up image folder import from xmind zen in yaml
   - This is a relative path (based on vault folder)
   - For example:
   
```yaml
---
mindmap-plugin: rich
xmind-image-target: xmind
---
```

## v1.5.5

Note: This is the first test version of MarkMind supporting Obsidian 0.15.0 pop out windows and some of the features aren't working as expected in the Obsidian pop outs yet

1. Fix #412
2. Fix #400

![test](https://user-images.githubusercontent.com/18719494/185738266-430f3103-f2e7-4712-8606-726ebc310fe1.gif)

## v1.5.2

1. Add layout for `rich` MindMap
2. Updated [Obsidian MarkMind docs](https://markmindckm.github.io/MarkMind-docs)

![1234](https://user-images.githubusercontent.com/18719494/179392911-6f526b3f-3b57-475a-973d-38e1446377a5.gif)

## v1.5.0

1. Fix #356
   - Now supports drag node to summary root in `rich` mode MindMap
2. Fix cannot delete node layout bug
3. Support batch delete nodes in `rich` mode
   - Use `Delete' and 'Backspace` key to delete node

![delete nodes](https://user-images.githubusercontent.com/18719494/172137807-f0aefce2-1f29-443a-94af-2f95138b6224.gif)

![rich](https://user-images.githubusercontent.com/18719494/171544455-650cd9c5-0fe4-4177-8d29-618ae2b76df0.gif)

## v1.4.5

1. Update to PDFJS [plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.4.5/PC.PDFJS.zip)
2. Support auto add to selected node or root of MindMap when annotating PDF on PC
3. Support drag nodes to another node
4. Fix #304
5. Fix #312

![test1](https://user-images.githubusercontent.com/18719494/166091478-4cd1883c-7adf-4b00-af70-7b85c26ae796.gif)

![test2](https://user-images.githubusercontent.com/18719494/166091482-ef936504-15a4-48ef-aca1-6c69028e23d8.gif)

## v1.4.4

1. Fix #280
2. Fix parse Obsidian callout bug
3. Tip:
   - Set color group on the settings tab to define the color of the node line
      - Examples: `red, orange, yellow, green, blue, #ccc,r gb(10,10,10)`
   - Set node color group to define board color when clicking on node

## v1.4.3

#### MindMap

1. Update to PC PDFJS [plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.4.3/PC.PDFJS.zip)
2. Fix #268, fix bug of `fish` layout in `rich` mode
3. Node support parse callout of Obsidian in `rich` mode

![callout](https://user-images.githubusercontent.com/18719494/162611444-eb67ab20-01cf-4da1-b19f-126a1c2808b9.gif)

#### PDF annotator

1. The short cuts have changed to this (Mac can also use)

| Feature             | Short Cut                       |
| --------------------| ------------------------------- |
| Highlight Yellow    | CTRL/CMD/ALT + Y                |
| Highlight Green     | CTRL/CMD/ALT + G                |
| Highlight Blue      | CTRL/CMD/ALT + B                |
| Highlight Pink      | CTRL/CMD/ALT + P                |
| Highlight Red       | CTRL/CMD/ALT + R                |
| Delete annotate     | CTRL/CMD/ALT + Delete/Backspace |

## v1.4.2

#### PDF annotate tool

1. Support annotate `http(s)`
2. You should ensure Obsidian can access the PDF file. For example:

```
---
annotate-type: PDF
annotate-target: https://mozilla.github.io/PDF.js/legacy/web/compressed.tracemonkey-pldi-09.PDF
---
```

3. Fix #253
   - When exporting highlight of PDF only keep color value
4. You can set the export PDF format in the settings at which point it can be used with admonition

```
Page:{{page}}
<span style="color:rgb({{color}})">■</span>:{{highlightText}}
Comment:{{comment}}
[📌]({{link}})
^{{id}}
```

#### MindMap feature

1. Support setup layout in YAML for `basic` mode
   - **Setup value `MindMap-layout` and `MindMap-layout-direct` at the same time!**

```
---
MindMap-plugin: basic
MindMap-layout: fish
MindMap-layout-direct: right
---
```

2. Now support layout and direct

| Layout  | Direct             |
|-------- | -------------------|
| MindMap | Right/Left/MindMap |
| Fish    | Right/Left         |

3. Support create hand drawn mode from `basic` mode
4. Support export to image but no support for edit mode in hand drawn mode
   - This is a testing feature and this feature will apply to `rich` mode only in the future
   - The default hand draw font is in `style.css`
   - In order to load the font you need internet access

```css
@font-face{
  font-family: 'myFont'; 
  src:url('http://cdn.ghost-jack.top/chinese.ttf');
}
.mm-handdraw-theme{
  font-family:'myFont';
}
```

5. You can change the font in `style.css` to your own. For example:

(Use `app://local/absolute font path` to load your local font which you would not need internet access for)

```css

@font-face{
  font-family: 'testFont'; 
  src:url('app://local/D:font/test.ttf');
}
.mm-handdraw-theme{
  font-family:'testFont';
}
```

![handdraw1](https://user-images.githubusercontent.com/18719494/161531764-31ec36cf-e102-45f9-adf2-7c93240ab38c.gif)

![下载 (1)](https://user-images.githubusercontent.com/18719494/161531939-b3c997e3-54ed-4d70-98fa-b6e00307bc93.png)

## v1.4.1

1. Fix #237
2. Fix #236
3. Fix MindMap scale bug
4. Support callout in `rich` mode
   - Supported on mobile and PC

![callout](https://user-images.githubusercontent.com/18719494/159688695-8d6fee36-29cb-4171-9b22-ae353a7e32fe.gif)

## v1.4.0

1. Update to PDFJS [plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/tag/1.3.9)
2. Fix #231
   - You can add a `link` variable in the settings tab when exporting PDF annotations

```
Page:{{page}}
<span style="color:{{color}}">■</span>:{{highlightText}}
Comment:{{comment}}
[📌]({{link}})
^{{id}}
```

3. Fix #174
   - Can now work directly with Obsidian Extended Table [plugins](https://github.com/aidenlx/table-extended)
   - When using `table` mode you can find `get markdown of this table` in the document menu options
   - Click it, then copy it to a md file, open table-extended plugin
   - **Note: Wrap is not supported in table mode**

```
---
MindMap-plugin: `basic`
display-mode: table
---
```

4. Support added for list mode parse `![[MindMap md]]` to a real MindMap
5. Fix `basic` mode MindMap parse `![[MindMap md]]` bug

##### Table mode with table extended plugin

![table](https://user-images.githubusercontent.com/18719494/158053432-d1956d65-a6e4-40fb-8003-0e757fe3b30d.gif)

##### Export PDF annotations

![highlight](https://user-images.githubusercontent.com/18719494/158053715-7c72d63c-93c0-4a53-9d2e-0014fb2c8086.gif)

## v1.3.9

1. Update to PC PDFJS [plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.3.9/PDFJS.zip)
2. Add a short cut `CTRL + C` to select text
3. Fix cannot click `copy` button bug when clicking on an annotation
4. Fix loss of `annotate-image-target` bug when saving PDF annotations

```
---
annotate-type: PDF
annotate-target: PDF/test.PDF
annotate-image-target: test/test
---
```

#### MindMap

1. Add scale button in MindMap
2. Fix #226
   - You can add `color` variable in settings tab when exporting PDF annotations

```
Page:{{page}}
<span style="color:{{color}}">■</span>:{{highlightText}}
Comment:{{comment}}
^{{id}}
```

![scale](https://user-images.githubusercontent.com/18719494/157392342-2372b4bd-8df9-4b84-9c18-6d1289cbea9b.gif)

![color1](https://user-images.githubusercontent.com/18719494/157392356-e1d97963-2665-43e7-b048-681d0a863429.gif)

## v1.3.8

1. Update to PDFJS [plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.3.8/PDFJS.zip)
2. Support search MindMap node
3. Add a menu `toggle search box` in `more options`
4. Fix #203
   - Support only copy PDF annotate text
5. Support micro adjustment of the height of the PDF annotate
   - You can add an upward or downward adjustment distance in the settings tab
6. Add a short cut `ALT + I` to `toggle create rect annotate status`
7. Fix #131
   - Support set up folder path for image of rect annotate in YAML
   - This is a relative path to a folder in your vault

```
---
annotate-type: PDF
annotate-target: PDF/test.PDF
annotate-image-target: test/test
---
```

#### Copy Text
![copyText](https://user-images.githubusercontent.com/18719494/156492427-e7a046e6-4782-4312-a03b-1e3ec98262a2.gif)

#### Add folder path for image of rect annotate

![imageFolder](https://user-images.githubusercontent.com/18719494/156492495-6ab436cb-4698-495c-9650-ee53622001c5.gif)

#### Adjust height of annotate

![adjustHeight](https://user-images.githubusercontent.com/18719494/156492522-322cdeb5-6a41-48ed-84c4-9ac9455efcf0.gif)

#### Search node

![search](https://user-images.githubusercontent.com/18719494/156496411-05d6afd8-6030-4878-819a-3cd07b479a22.gif)

## v1.3.7

1. Update to Mobile PDFJS [plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/tag/1.3.6)
2. Add command to toggle version of PC PDFJS plugin in command board `CTRL + P`
3. Update PC PDFJS [plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.3.7/PDFJS.zip)
   - Support old and new version（#197）
   - Support highlight text by use shortcut key `ALT + Y/R/G/P/B`
   - Fix #197
      - In rare cases, due to a problem with the PDF format, there will be problems in the text selection of the new version
      - You can use the old version to solve this issue
      - Generally, please use the new version as it has a better experience overall

![PC PDFJS](https://user-images.githubusercontent.com/18719494/154829513-224a003d-5892-49b3-ba02-f39e72557ce6.gif)

## v1.3.6

1. Update to mobile PDFJS [plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.3.6/mobile.PDFJS.zip)
2. Fix #196
3. Fix #184

https://user-images.githubusercontent.com/18719494/154784360-9a502fe8-843c-416f-8d56-b895bdad6399.mp4

## 1.3.5

1. Fix #159
2. Support creating `rich` mode from `basic` mode
   - You can use `CTRL + P` and then click the `change basic` to `rich` mode command
3. Support `Import highlight annotations from PDF`
   - You can find a menu option for this in `more options` when opening a PDF
4. Support export of PDF annotations as a format
   - You can find a menu option for this in `more options`
   - You can configure the format in the setting tab
   - The default format is:

```
Page:{{page}}
Text:{{highlightText}}
Comment:{{comment}}
^{{id}}
```

![123456](https://user-images.githubusercontent.com/18719494/153592129-842da678-cd8d-46fe-8df6-8c7238d0f583.gif)

![1234567](https://user-images.githubusercontent.com/18719494/153592138-c4899a71-cc4d-4f68-9707-fdddd4a228f3.gif)

![12345678](https://user-images.githubusercontent.com/18719494/153593116-5a725dfc-70f0-4a17-a9ad-3c2bccb70f99.gif)

## 1.3.4

1. Reconstruct PDF annotation
   - This is only for the PC version of the [PDFJS plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.3.4/PDFJS.zip)
2. Optimize some mind mapping functions

![PDF](https://user-images.githubusercontent.com/18719494/152282005-8f00b132-018d-4154-b4b9-0b4d334623a7.gif)

![pdftest](https://user-images.githubusercontent.com/18719494/152311838-05ffdbb4-3040-4a82-afd5-f0165bb016df.gif)

## v1.3.3

1. Update to PDFJS [plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.3.2/internal-PDFJS.zip)
2. Support changing related link of node
   - Now support line/polyline/Bessel curve
3. Support adding a theme
4. Support for white board

```
---
MindMap-plugin: rich
MindMap-theme: whiteboard
---
```

![11](https://user-images.githubusercontent.com/18719494/150154942-6a62497b-2264-4435-9d05-4cd421455b76.gif)

![12](https://user-images.githubusercontent.com/18719494/150155333-5e3b06c6-5620-4121-9adb-c3f976774d84.gif)

![13](https://user-images.githubusercontent.com/18719494/150158918-3ac0b308-7745-4dbb-bab5-715ccc9d1c5c.gif)

## 1.3.2

1. Update to PDFJS [plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.3.2/internal-PDFJS.zip)
   - Manually download internal [Obsidian MarkMind](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.3.2/internal-Obsidian-MarkMind.zip)
2. Fix parse ![[MindMap md]] in `table` mode
3. Fix parse ![[table mode MindMap md]] to real table in node of MindMap/markdown file
4. Fix export table mode MindMap to html
5. Fix #157
6. Support create free node
   - The text is `![[file name]]` when dragging a file in the vault to `rich` mode
   - Support extension md/png/gif/jpg
7. Support `Get markdown table` added in `options` when in table mode
8. Fix #99
   - Support PC PDFJS `import existing PDF highlights`
   - Find in the `more options` menu for the document

### Internal test function, allow only purchased users to use

![11](https://user-images.githubusercontent.com/18719494/149620970-f3556f46-33bf-434f-b99e-3d6ff72bd2d6.gif)

![12](https://user-images.githubusercontent.com/18719494/149620976-2bc3702d-2f32-4f7f-a7a2-ee57d832fb8f.gif)

### Internal test function

![import](https://user-images.githubusercontent.com/18719494/149621321-45664041-e40f-4599-a25e-bdc39e977a28.gif)

## 1.3.1

Making table in markdown is very troublesome, so `table` mode is added to `basic` mode for better ease

- You can add `display-mode: table` in `basic` mode
- Or you can find `open as table` in `more options`
- Support get table html code
   - You can find `get table html` in `more options` when in `table` mode
- Support `Enter' and 'Tab` short cut
- Support editing text by double clicking
- You can change node position in `MindMap` mode
- **Drag and drop is not supported**

<pre>
---
MindMap-plugin: basic
display-mode: table
---
</pre>

![table](https://user-images.githubusercontent.com/18719494/148937281-3ff868b3-ccb6-404e-8f37-14b8e153feb5.gif)

![table1](https://user-images.githubusercontent.com/18719494/148937290-55fa7630-65d3-4b62-9e24-978f0de4c180.gif)

## 1.3.0

1. Fix #152
2. Fix #150
3. Fix #149

## v1.2.9

1. Add a layout `vertical time`
   - The short cut is `CTRL + K`
2. Add a layout `fish right`
   - The short cut is `CTRL + Q`
3. Add a layout `fish left`
   - The short cut is `CTRL + T`
4. Previous projects have been completed
   - Plan for this year: https://github.com/MarkMindCkm/Obsidian-MarkMind/projects

![fish1](https://user-images.githubusercontent.com/18719494/148394155-8fb4007e-6061-4ea3-8693-d27bbc036f33.gif)

## v1.2.8

1. Fix parse `![[MindMap md name]]` bug when node has image
2. Fix style of node

## v1.2.7

1. Fix #138
2. Fix #130
3. Fix #129
   - Support parse `![[MindMap md name]]` to MindMap in MindMap node
4. Fix #124
   - Support parse `![[MindMap md name]]` to MindMap in md file

![test](https://user-images.githubusercontent.com/18719494/147801351-23842bd9-af20-4589-9459-774618bd5dac.gif)

![test1](https://user-images.githubusercontent.com/18719494/147801356-3edca7dc-d0ea-4213-9974-a37f71aa438c.gif)

![test2](https://user-images.githubusercontent.com/18719494/147801360-ed8aba1d-3dcf-4b97-a7a0-6dfc41597cd1.gif)

## v1.2.6

1. Add more options for canvas size in settings tab
2. Optimize the logic of the pop-up node setting box
3. Support export MindMap to html
   - Use `CTRL + P` then you can find the export to html command

Note:
   - Blank links `![[svg/PDF/mp4]]` and mobiles are not supported
   - Only `![[png/jpg]]` images are supported in the node
   - Image in MindMap must be local
   - Support export mathematical formula
   - If the MindMap is too large it cannot be exported
   - The max export size is 16384 X 16384 (pixel)

![1234](https://user-images.githubusercontent.com/18719494/147195606-3a270e5e-2628-4322-bd87-9ef6d1004b66.gif)

## 1.2.5

1. Optimize the interaction of node setting box
2. `CTRL/CMD + Mouse click` to select nodes
   - Right click not supported
3. Add Mac PDFJS plugin path

## 1.2.4

1. Right click to select nodes and left click to move the MindMap
2. In `rich` mode, support set up node background/stroke/text color/text size
3. If you want to change colors of the node setup board you can input the setup board color in the settings tab
   - Afterwards please restart Obsidian

## 1.2.3

1. Fix v1.2.2
   - Tab/Enter bug

## v1.2.2

1. Fix #108
2. Fix #103
3. Add `copy and paste` command `CTRL + P`
4. Support copy and pasting node on mind maps
5. Optimize input
   - Select the node, press spacebar to edit the node in append mode, and press other keys to edit in overwrite mode

## v1.2.1

1. Update to PDFJS [plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/tag/1.2.0)
2. Fix set up PDFJS plugin bug
3. Epub support added on PC

## v1.2.0

1. Update to PDFJS plugin
   - [PC PDFJS plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.2.0/PDFJS.zip)
   - [Android PDFJS plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.2.0/Android.PDFJS.zip)
   - [IOS PDFJS plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.2.0/ios.PDFJS.zip)
2. Fix #87
3. Support read and annotate epub file
   - This is currently a beta function
4. Fix miss `$` when save data bug
5. Simplify set up for mobile PDFJS plugin path

#### Epub YAML

```
---
annotate-target: test.epub
annotate-type: epub
---
```

You can find `annotate epub` in `more options`

## v1.1.9

1. Update to IOS PDFJS [plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.1.9/ios.PDFJS.zip)
2. Fix cannot use highlight text in IOS system
3. Support parse code block in markdown file
   - You should open it in the settings tab and restart Obsidian

## v1.1.8

1. Update to PDFJS [plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.1.7/PDFJS.zip)
2. Support a new layout in `rich` mode of MindMap
   - The short cut is `CTRL/CMD + J`
3. Support import xmind zen file in `rich` mode of MindMap
   - You can do this by dragging and dropping the xmind zen file into blank space of the MindMap in `rich` mode
4. Fix some times can not add/remove free node bug
5. Use `CTRL + J` to change to new layout

#### Demo

This is a xmind zen [demo](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.1.8/note.taking.1.xmind)

Import xmind zen file
![note 12367133](https://user-images.githubusercontent.com/18719494/141953779-f7e1fdf2-8e0f-4ab0-b099-7d5bfb7a07f5.gif)

![note 12367133tt](https://user-images.githubusercontent.com/18719494/141953811-9657cf8d-e04e-4c7b-8499-154f9e3272d5.gif)

## v1.1.7

1. Update to PC PDFJS [plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.1.7/PDFJS.zip)
2. Fix `basic` mode can add free node bug
3. Fix annotate export to PDF in PC version

## v1.1.6

1. Update to PC PDFJS [plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.1.6/PDFJS.zip)
2. Fix #60
   - Add PDF annotate short cut
3. Fix #61
4. Fix #64
5. Fix #66
6. MindMap node support for smooth movement which is in the settings tab
7. In `rich` mode of MindMap, you can add a free node when double clicking the blank space
8. Fix #57

| PDF annotate feature | Short Cut                       |
| -------------------- | ------------------------------- |
| Highlight Yellow     | ALT + Y                         |
| Highlight Green      | ALT + G                         |
| Highlight Blue       | ALT + B                         |
| Highlight Pink       | ALT + P                         |
| Highlight Red        | ALT + R                         |
| Delete annotate      | ALT + Delete/Backspace          |

![note 1236](https://user-images.githubusercontent.com/18719494/140644085-fc8c9f2e-d058-4ff5-a436-7edd58e33b42.gif)

## v1.1.5

1. Update to PDFJS plugin
   - [PC PDFS plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.1.6/PDFJS.zip)
   - [Android PDFJS plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.1.0/mobile.PDFJS.zip)
   - [iPhone/iPad PDFJS plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.1.9/ios.PDFJS.zip)
2. Support adding note to MindMap node in `rich` mode
3. Summary node support add child node
4. `CTRL + P` add a command `get base path of vault`
   - It will auto copy to clipboard

![note](https://user-images.githubusercontent.com/18719494/139576838-812bf0c5-84e5-452e-accb-738517ebe7a9.gif)

![123421](https://user-images.githubusercontent.com/18719494/139576842-3a2293a5-8238-4eb6-8475-1071ee5f14f5.gif)

## v1.1.4

1. Fix delete summary bug when editing node and using backspace/delete key

## v1.1.3

1. Fix #54
2. Fix #28
3. Fix missing code and link bug in outline mode

## v1.1.2

1. Fix #46
2. Add `set MindMap to center` menu in `more options`

## v1.1.1

1. Update to PDFJS plugin
   - **Mobile PDFJS plugin needs to be downloaded again**
   - [PC PDFJS plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.1.6/PDFJS.zip)
   - [Android PDFJS plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.1.0/mobile.PDFJS.zip)
   - [iPhone/iPad PDFJS plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.1.1/ios.PDFJS.zip)
2. Fix iPhone/iPad cannot use PDF annotate bug

Notes:
   - Please set up PDFJS path in the MarkMind settings tab
      - This is an absolute path
      - You can find the absolute path of your vault in Obsidian app
      - The best way to find the path is to create a folder (such as `plugin`) in your vault and then put the PDFJS plugin into it

#### About iPhone/iPad PDFJS path

1. Create a `plugin` folder in your vault, then put `PDFJS plugin` into it
2. The path will like this:
   - `/var/mobile/Containers/Data/Application/FACF6387-DAA2-45B3-8F52-3536E1EC29A1/Documents/plugin/PDFJS`
   - The folder `FACF6387-DAA2-45B3-8F52-3536E1EC29A1` is different on each device

#### About Android PDFJS path

1. Create a `plugin` folder in your vault and then put PDFJS plugin into it
2. The path will look look like this:
   - `/storage/emulated/0/Documents/Obsidian/Obsidian/plugin/PDFJS`

#### About PC PDFJS path

1. Create a `plugin` folder in your vault and then put PDFJS plugin into it
2. The path will look like this:
   - `D:\plugin\PDFJS`

iPad screen short
![68747470733a2f2f692e6c6f6c692e6e65742f323032312f31302f31312f3431557933536d756a4b723835515a2e706e67](https://user-images.githubusercontent.com/18719494/136878933-3c86d930-e2fd-4dd4-8c1e-8c4de6cc1ac7.png)

## v1.1.0

1. Update to PDFJS plugin
   - [PC PDFS plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.1.7/PDFJS.zip)
   - [Android PDFJS plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.1.0/mobile.PDFJS.zip)
   - [iPhone/iPad PDFJS plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.1.1/ios.PDFJS.zip)
2. Fix #40
   - You can select the MindMap mode (when creating a MindMap) in the settings tab
   - The default is `basic`
2. PDF annotate support for mobile
   - Only supports PDF in your vault, not `file://`
3. In an md file, support for use of `[[md#^node id]]` to reference a node of a `rich` mode MindMap
   - You can find `copy node id` in the `more options` menu
4. Support image folder in settings tab to save image of PDF rect annotations
5. Fix when annotate `file:// PDF path` cannot use rect annotate bug
6. Support 3 themes in MindMap
7. You can add YAML to markdown

#### PDFJS Setup

1. You should set the PDFJS plugin path in the MindMark settings tab
   - It is an absolute path
   - For example: 
     - `D:plugins/PDFJS` on PC
     - `/storage/emulated/0/Documents/Obsidian/Obsidian/plugin/PDFJS` on Android
2. You should put PDFJS plugin into an accessible folder on mobiles
3. The best way to find the path is to create a folder (such as `plugin`) in your vault and then put the PDFJS plugin into it

#### Theme example

```
---
MindMap-plugin: basic (or rich)
MindMap-theme: dark (or light or card)
---
```

<img src="https://user-images.githubusercontent.com/18719494/136696974-a776ad2c-aab5-4d62-917f-2b294d1da40a.gif" width="300"/> <img src="https://user-images.githubusercontent.com/18719494/136696996-36cd0e77-8212-4b6f-8f55-6dbf617cf906.gif" width="300"/>

![动画1211713467](https://user-images.githubusercontent.com/18719494/136694951-9bb9720d-b5e3-4622-8929-70de6fb7f24a.gif)

## v1.0.9

1. Fix #4
   - PDF annotate support all PDF files on disks by using `file://`
   - This feature can only be used on the desktop app
   - If you use `file://` the annotations will be saved to this markdown file
   - Example YAML:

```
---
annotate-target: file://PDF absolute path
annotate-type: PDF
---
```

2. Fix #29
   - Support for mobile
3. Add command:
   - Select node, change layout in `rich` mode of MindMap
   - Toggle markdown and MindMap mode
4. Add some menus of `more options` in `rich` mode of MindMap (copy text to clipboard automatic)
   - Copy node text as markdown (contains children)，the text type like `basic` mode
   - Copy node text (only this node)
   - Copy node links which you can reference it in other md file
5. Support change summary/boundary/related link color
6. If you set up active code in the settings tab the desktop version will create mobile active code in your Obsidian-MarkMind plugin `json` file automatically
7. Support moving root of MindMap in `rich` mode

![12117](https://user-images.githubusercontent.com/18719494/135819440-34380383-0a3a-481c-b5ac-205f6a9da155.gif)
<img src="https://user-images.githubusercontent.com/18719494/135823093-f34d6870-7dfb-4646-8874-1347ad5047f0.gif" width="300"/>

## v1.0.8

1. Fix #26
2. Fix missing markdown format in `list` mode when using `CTRL + Down/Up`

## v1.0.7

1. Update to PDFJS plugin
   - [PC PDFS plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.1.7/PDFJS.zip)
   - [Android PDFJS plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.1.0/mobile.PDFJS.zip)
   - [iPhone/iPad PDFJS plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.1.1/ios.PDFJS.zip)
2. Fix #24
   - Fix PDF multi line select to highlight
   - This problem is caused by the PDF plugin

## v1.0.6

1. Emergency fix #22
2. Emergency fix #21

## v1.0.5

1. Emergency fix for MindMap `rich` mode bug

## v1.0.4

1. Update to PDFJS [plugin](https://github.com/MarkMindCkm/Obsidian-MarkMind/releases/download/1.0.7/PDFJS.zip)
2. Fix #18
   - You can select the PDF viewer theme in setting tab
3. Fix #17, #15, and #8
4. Support opening multiple PDF annotate and adding comments to annotation
5. Support committing highlights and notes to PDFs
   - You can find the `export PDF annotate` option in `more options`
   - It will create a file in your folder named `${PDF name}-annotate.PDF`
6. Split PDF annotation and MindMap function
7. In `basic` mode, changed MindMap layout from `tree` to `MindMap`
8. Fix #2
   - In `rich` mode:
     - If this is the first time saving data it will output as markdown
     - If it is not the first time to save data it will only replace `${MindMap data}`
     - If you want to reference a node it will automatically create a MindMap node reference link
     - Can copy to your clipboard when clicking node and pressing `CTRL` or `Command`

#### Rich format example

```
---
MindMap-plugin: rich
---

# title
 json
  ${MindMap data}
```

The use of PDF annotation has changed. If you want to use the annotate function, you can add this `yaml` to your markdown file:

```
---
annotate-target: test/test.PDF
annotate-type: PDF
---
```

- In the MindMark settings tab, you can select the `md` or `annos` format to save annotations
   - `annos` is the default type
      - It is formatted as a `json` file
	  - You can use `Obsidian://jump-to-PDF` to reference annotations
      - Annotations do not contaminate MD files when referenced
   - `md` is the recommended way 
      - You can use `Obsidian://jump-to-PDF` to reference annotations
      - Or you can use `![[md#^block id]]` to reference annotations
