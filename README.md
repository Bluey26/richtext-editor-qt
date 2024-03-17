# rich-editor-qt

![example](https://github.com/Bluey26/rich-editor-qt/assets/143142826/7274045a-13d1-417b-b659-42c99cb1993c)


WYSIWYG lightweight Rich text editor example code used to demonstrate the capabilities of Qt's QTextEdit class. Allows to write and see markdown,html and plaintext. Allows to export to .odt and .pdf


This code has been obtained from:
https://doc.qt.io/qt-5/qtwidgets-richtext-textedit-example.html which links to the original code: https://code.qt.io/cgit/qt/qtbase.git/tree/examples/widgets/richtext/textedit?h=5.15

---
This program has a few changes respect to that code, including:

- The removal of the example.html file being opened every time the program is opened.

- Fixed 'Save as' format handling. Original code seems to save as .odt by default.

- Allow to load files from terminal command arguments, whichs also allows you to customize 'open with' files which can be opened with this small program.(So you can use it as a normal text editor)


To compile the program in linux, you have to run the following commands in the project folder:

```
qmake

make
```

After that you will have a `textedit` binary which you can link to certain file formats.

**To see an introduction of the program capabilities, open example.html or example.md using the program.**

At the moment, the program can write/open the following formats:
- .TXT
- .MD (Markdown)
- .HTML *

* HTML is written using QTextDocument rich text, which is based in HTML4 markup (More info in: https://doc.qt.io/qt-6/richtext-html-subset.html). It tends to add some unnecesary code, so using markdown is recommended.




The program is also able to export to the following formats (But at the moment cannot open them):

- .ODT (Open Document Text)
- .PDF (Portable Document Format)

Unfortunately it is not able to open and edit the .odt and .pdf created with this program.

There are still some things to do, like:
- adding strikethrough button.
- A button to add images
- Zoom-in and zoom-out capabities
- Being able to resize images
- Link button and automatic link detection
- Paste without formatting
- Bulletlist and ordered list button
- Paste date and time shold not paste into the last line, but in the line the cursor is located


---
License: GPL v3
