# summernote-pagebreak

This Plugin adds a Page-Break button to the Summernote toolbar that when used adds page-breaks for printing. The editor will show where your page-breaks are, but using the styles below they won't show on pages, but will work when printing the page.
By selecting, or highlighting the block of text you want the page-break to appear after will insert a page-break div after the selected area. If used without selecting a content section will place the page-break at the end of the content.

### Installation

#### 1. A note for using this plugin.
In your main CSS for where the page-break/s will be used, you'll need to make sure that the below is included in your stylesheet.
The first declaration ensures that the page-break is never seen visually on your page, while the second ensures that the page break is seen by the printer.

````css
@media all {
	.page-break	{ display: none; }
}

@media print {
	.page-break	{ display: block; page-break-before: always; }
}
````

#### 2. Include JS

Include the following code after Summernote:

```html
<script src="summernote-pagebreak.js"></script>
```

#### 3. Supported languages

Currently available in English!

#### 4. Summernote options

```javascript
$('.summernote').summernote({
    toolbar:[
        ['pagebreak',['pagebreak']], // The Button
        ['style',['style']],
        ['font',['bold','italic','underline','clear']],
        ['fontname',['fontname']],
        ['color',['color']],
        ['para',['ul','ol','paragraph']],
        ['height',['height']],
        ['table',['table']],
        ['insert',['media','link','hr']],
        ['view',['fullscreen','codeview']],
        ['help',['help']]
    ],
});
```

#### 5. Check out our other Summernote Plugins via our main Github page.
- [Diemen Design](https://github.com/DiemenDesign/)
