# obsidian mark mind

Obsidian mark mind is a mind map , outliner and pdf annotate tool base on obsidian api.

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
| Change mindmap layout                   | Ctrl/Cmd + U / D / L / R / M |
| delete summary / boundary / relate link | Delete/Backspace             |


## There are tow types to save pdf annotation,the default is  use `annos` file to save annotations,the other ways is use `md` file to save annotations

### how to use pdf annotate

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


### demonstration

#### `obsidian://jump-to-pdf`
![1](https://user-images.githubusercontent.com/18719494/130034457-f9f44170-6030-4179-b59f-21d4035c82c7.gif)

![2](https://user-images.githubusercontent.com/18719494/130034688-496d8156-d4c5-4764-bc4e-a9e0d7e2a499.gif)

![3](https://user-images.githubusercontent.com/18719494/130034968-7e8ff685-7ce7-4bd8-aa11-f8e7fd71bbf0.gif)

![4](https://user-images.githubusercontent.com/18719494/130035036-fe5394ed-8e18-4e3e-922e-81674f132061.gif)

#### Markdown file of annotations
![1](https://user-images.githubusercontent.com/18719494/131444787-c6168197-ecd6-4b20-a134-39eb54c47d90.gif)
![2](https://user-images.githubusercontent.com/18719494/131444872-6b11111d-48de-462d-b96a-d468a0aeb8ef.gif)


## outline

## In `basic` mode

You can add yaml to active outline mode:

``` 
---

mindmap-plugin: basic
display-mode: outline

---

```

### Outline short cut

| Features             | Short Cut                       |
| -------------------- | ------------------------------- |
| New Brother Node     | Enter                           |
| Indent               | Tab                             |
| Unindent             | Shift+Tab                       |
| Zoom in              | Ctrl/Cmd+] Or Double Click Dott |
| Zoom out             | Ctrl/Cmd+[                      |
| Move Up Or Down Node | Ctrl/Cmd + up/down              |






