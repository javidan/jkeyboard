
![jKeyboard](http://javidan.github.io/jkeyboard/images/keyboard.jpg)

This is simple jQuery on screen keyboard.

usage:

    <script src="http://code.jquery.com/jquery-1.10.1.min.js"></script>
    <script src="jkeyboard.js"></script>
    <link rel="stylesheet" href="jkeyboard.css">
 
    <input type="text" id="search_field">
    <div id="keyboard"></div>


    $('#keyboard').jkeyboard({
      layout: "english",
      input: $('#search_field')
    });

[Click to view in action](http://javidan.github.io/jkeyboard/examples/index.htm) 

for now new layouts can be added on jkeyboard.js, I'm working on basic api.

Example layout for russian:

    russian: [
        ['й','ц','у','к','е','н','г','ш','щ','з', 'х' ],
        ['ф','ы','в','а','п','р','о','л','д','ж', 'э' ],
        ['shift','я','ч','с','м','и','т','ь','б','ю', 'backspace'],
        ['numeric_switch','layout_switch', 'space','return']
    ],