
![jKeyboard](http://javidan.github.io/jkeyboard/images/keyboard.jpg)

[See In Action](http://javidan.github.io/jkeyboard/examples/index.htm)


# JKeyboard

A simple jQuery on screen keyboard.
## Feautures
- Easy Setup
- Switch layout on the Fly
- Supports multiple input fields
- Custom layout

## 1. Getting Setup

#### 1.1. Installation

- First, copy and paste `lib/js/keyboard.js` in your project, and link to it before the closing `</body>` element. Make sure jquery is linked before this.
- Next, you'll need to copy and paste the plugin's css into your project. Both Scss and Css are included for flexibility and modifications.
- Lastly, link to the keyboard css file `jkeyboard.css` file before the closing `</head>` element.

Note: This plugin requires your website or application already runs a copy of [jQuery](http://jquery.com/), version 1.10.1 or higher.


    <script src="http://code.jquery.com/jquery-1.10.1.min.js"></script>
    <script src="jkeyboard.js"></script>
    <link rel="stylesheet" href="jkeyboard.css">
 
#### 1.2 The Basics

The first thing you will require is a keyboard holder that will hold the keyboard, and an input field on which the keyboard will operate.

```
<input type="text" id="search_field">
<div id="keyboard"></div>
```
```           
$('#keyboard').jkeyboard({
    input: $('#search_field')
});
```

#### 1.2 Configuration

To configure custom options when you initialize jKeyboard, simply pass an object in your call to jkeyboard:


##### 1.2.1 Simple Example
```
$('keyboard').jkeyboard({
    input: $('#search_field),
    layout: 'english'
});
```
##### 1.2.2 Options

Option             |type           | Default   |values| Description              
-------------------|---------------|-----------|------|--------------------------------------
`customLayouts`     |object| `{selectable:[]}`  |`selectable,` `customLayoutName`| All the custom layouts as well as custom selectable layouts are defined in this object.
`customLayouts.selectable` | array|`[]`         || array of selectable custom layouts. If you have more than one custom layout, you can choose which layout to show in the layout switch.
`customLayouts.layoutname` | an array of keys for keyboards  |`[]`|| You can add as many custom layouts as you wish in the format of customLayouts.layoutName. Ex. <br> <pre>russian: [<br>   ['й','ц','у','к','е','н','г','ш','щ','з', 'х' ],<br/>   ['ф','ы','в','а','п','р','о','л','д','ж', 'э'],<br/>    ['shift','я','ч','с','м','и','т','ь','б','ю', 'backspace'],<br>    ['numeric_switch','layout_switch', 'space','return']<br>]</pre> [Click to view in action](http://javidan.github.io/jkeyboard/examples/index.htm) 


##### 1.2.3 Methods
Method             |type           |values| Description              
-------------------|---------------|------|--------------------------------------
`init`     |object| `layout`<br> `input` <br>`customLayouts`| All the custom layouts as well as custom selectable layouts are defined in this object.
`setLayout`|string|`azeri`<br/>`english`<br/>`russian`<br/>`numeric`<br/>`numbers_only`<br/>`symbolic`<br/>`*custom layout names*`<br/>
