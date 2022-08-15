# Obsidian Markmind

The Obsidian Markmind Pluigin is a mind map, outliner, and PDF annotation tool that uses the Obsidian API.

## Mind Map Shortcuts

| Create New Mind Map                      | Ctrl/Cmd + P                       |
| ---------------------------------------- | ---------------------------------- |
| Create New Child Node                    | Tab                                |
| Create New Sibling Node                  | Enter                              |
| Delete Node                              | Delete / Backspace                 |
| Edit Node                                | Space / Dbl Click Node             |
| Undo                                     | Ctrl / Cmd + Z                     |
| Redo                                     | Ctrl / Cmd + Y                     |
| Quit Edit Node                           | Tab                                |
| Expand Node                              | Ctrl / Cmd + /                     |
| Collapse Node                            | Ctrl / Cmd + /                     |
| Move Node To Another Node                | Drag & Drop Node                   |
| Tab Node                                 | Up / Down / Left / Right           |
| Zoom In / Out                            | Ctrl / Cmd + Scroll Up / Down      |
| Center Mind Map                          | Ctrl / Cmd + E                     |
| Change Mind Map Layout                   | Ctrl / Cmd + U / D / L / R / M / J |
| Delete Summary / Boundary / Related Link | Delete / Backspace                 |

---

## PDF Annotator

### How To Save PDF Annotations

There are two ways to save pdf annotations:
   1. The default method is with the ` .annos ` file extension.
   2. The other method is with the ` .md ` file extension.

### How To Use The PDF Annotator

1. You first will need to download the [PDF JS Plugin](https://github.com/MarkMindCkm/obsidian-markmind/releases/download/0.1.2/pdfjs.rar).
2. Open the Setting Tab inside your Obsidian App to set up the PDF Plugin Path:
      - example: ` D:plugins/pdfjs `
      - The path needs to be an absolute path
4. Open any file as a Mind Map.
5. Use ` [[]] ` to make PDF Reference.
6. Click PDF Reference, which will open a PDR reader if the PDF Plugin path has properly configured.
7. Use PDF Annotate function:
   - By default this will create a ` .annos ` file in your folder where the annotation data will be saved. Although it uses the ` .annos ` file extension, this file is in fact a ` .json ` file.
   - If you select (save PDF annotation type ) ` markdown ` in setting tab , it will create a ` ${pdf name}-annotate.md ` file in your folder. Each annotation has an associated quote block with a block reference. **DO NOT manually modify these blocks.**
   

### How To Relate Mind Map Nodes And Annotations

There are three ways to relate Mind Map Nodes and Annotations:

1. Default:
   -  Make a PDF annotation.
   -  Click PDF annotate.
   -  Edit a Mind Map Node , and press ` Ctrl / Cmd + v ` to relate node and annotate.
   -  Clicking Node PDF annotate mark will auto copy the ` id ` of an annotation to the clipboard.

2. Use The Protocol Support ` obsidian://jump-to-pdf: `
   -  Open protocol support in setting tab.
   -  Automatic create PDF annotation reference link and copy to clipboard when click pdf-annotate.
   -  Paste to markdown file.

3. Use Markdown To Save PDF Annotations:
   -  You can use ` [[${md name}#${block reference}]] ` to associate quote block with a block reference.
   -	An obsidian link to an annotation block-reference will, when clicked, open the corresponding file and scroll to the associated highlight. If the file is already open in a pane, then the link will cause the existing pane to scroll instead.


## Demonstration

### ` obsidian://jump-to-pdf `

![1](https://user-images.githubusercontent.com/18719494/130034457-f9f44170-6030-4179-b59f-21d4035c82c7.gif)

![2](https://user-images.githubusercontent.com/18719494/130034688-496d8156-d4c5-4764-bc4e-a9e0d7e2a499.gif)

![3](https://user-images.githubusercontent.com/18719494/130034968-7e8ff685-7ce7-4bd8-aa11-f8e7fd71bbf0.gif)

![4](https://user-images.githubusercontent.com/18719494/130035036-fe5394ed-8e18-4e3e-922e-81674f132061.gif)

### Markdown File Of Annotations

![1](https://user-images.githubusercontent.com/18719494/131444787-c6168197-ecd6-4b20-a134-39eb54c47d90.gif)
![2](https://user-images.githubusercontent.com/18719494/131444872-6b11111d-48de-462d-b96a-d468a0aeb8ef.gif)


## Outline Mode

### In ` basic ` Mode

You can add yaml to active outline mode:

``` 
---

mindmap-plugin: basic
display-mode: outline

---

```

### Outline Mode Shortcuts

| Features             | Shortcut                        |
| -------------------- | -------------------------------- |
| New Sibling Node     | Enter                            |
| Indent               | Tab                              |
| Outdent              | Shift + Tab                      |
| Zoom In              | Ctrl/Cmd + ] Or Double Click Dot |
| Zoom Out             | Ctrl/Cmd + [                     |
| Move Up Or Down Node | Ctrl/Cmd + Up / Down             |

