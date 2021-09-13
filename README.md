
# Obsidian mark mind

## Introduction

Obsidian mark mind is a mind map and pdf annotate tool base on obsidian api.

## Mind map introduction

it contains  two modes : basic and rich 

The yaml :

```yaml
---

mindmap-plugin:basic (or rich)

---
```

In the basic mode , you can only use the basic mind map function , it is the obsidian-enhancing-mindmap plugin.

In the rich mode , you can use all functions of mind map and pdf annotate function.

- summary
- boundary
- node relate link
- free node

### Rich mode will output  this  markdown:

```markdown
---

mindmap-plugin:rich

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

### step

1. You need download pdf js plugin , download this [pdf js plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/0.1.2/pdfjs.rar)
2. Open setting tab  to set up pdf plugin path , for example:D:plugins/pdfjs , It is a absolute path
3. Open as mind map
4. Use `[[]]` to reference pdf
5. Click pdf reference , it will open a pdf reader if pdf plugin path is correct
6. Use pdf annotate function 
   - it will create `annos` file in your folder as default, the `annos` file store annotations data,`annos` file is a `json` file in fact
   - if you select (save pdf annotation type ) `markdown` in setting tab , it will create `${pdf name}-annotate.md` file in your folder. Each annotation has an associated quote block with a block reference. please do not  modify these blocks
   

### how to relate mind map node and annotate?

There are three ways to  relate mind map node and annotate

#### Default

- make a pdf annotate
- click pdf annotate
- edit mind map node , `ctrl/cmd + v` to relate node and annotate
- click node pdf annotate mark will auto copy `id` of annotate to clipboard


#### Support `obsidian://jump-to-pdf` protocol

- open protocol support in setting tab
- automatic create PDF annotation reference link and copy to clipboard when click pdf-annotate
- paste to markdown file

#### If you use markdown to save pdf annotations

-	you can use `[[${md name}#${block reference}]]` to associate quote block with a block reference.
-	An obsidian link to an annotation block-reference will, when clicked, open the corresponding file and scroll to the associated highlight. If the file is already open in a pane, then the link will cause the existing pane to scroll instead.
### Demonstration

<img src = 'https://user-images.githubusercontent.com/18719494/130031749-84b84833-a52c-4ad1-b589-00eb2d8af317.gif' width="800px">

## Notice 

This is not an open source project , It is currently in beta .
Web site : https://www.markmind.net

## Donating
<a href="https://www.buymeacoffee.com/markmind"><img src="https://img.buymeacoffee.com/button-api/?text=Buy me a coffee&emoji=&slug=markmind&button_colour=FFDD00&font_colour=000000&font_family=Cookie&outline_colour=000000&coffee_colour=ffffff"></a>


