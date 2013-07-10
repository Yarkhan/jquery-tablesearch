# jQuery Table Search 

Query into an html `table`

## Usage

Include jQuery and Table Search

```html
<script src="jquery.js"></script>
<script src="tablesearch.jquery.js"></script>
```

Call the plugin. Usually you would have an `input` and get
its value compared to the `table` to get the results.
The results that do not match `input` will `fadeOut()`.

```javascript
$('#myInput').keyUp(function(){
  $('#myTable').tableSearch($(this).val())  ;
});
```

That's all.
What? Do wanna more? Your greedy bastard.


## Options

You can also pass an object as second parameter with the callback 
functions, so you can do literally anything with the results.

```javascript 
//Instead fading, let's just change their background
$('#myInput').keyUp(function(){
  $('#myTable').tableSearch($(this).val(),{
    withMatch:  function(matches){
      matches.css('background','gray');
    },
    withNoMatch: function(nomatches){
      nomatches.css('background','white');
    }
  });
});
```

## License

[WTFPL License](http://www.wtfpl.net/txt/copying/)
