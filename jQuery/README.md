# jQuery LectureNote (Basic)

## jQuery 기능삽입
코드 안에 어떻게 jQuery기능을 포함시키는지.
- Method1: 
	+ `<script src="jquery-3.2.1.min.js"></script>`
	+ 이렇게 해당 폴더안에 jQuery파일들을 포함해서 작동시키는게 조금더 안정적
- Method2:
	+ `<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>`

## Selector
`$("#mijeong")`

## onclick
`$("#circle").click(function() { ... });`

## innerHTML
- text 바꾸기: `$("p").html("This text has changed!");`
- text 내용 return: `alert($("p").html());`

## hover
`$("#circle").hover(function() { ... });`

## Change attributes 
````js
$("#circle").hover(function() {
        $("iframe").attr("src", "https://www.ecowebhosting.co.uk");
});
````

## Change CSS
````js
$("#circle").click(function() {
        $("#circle").css("width", "400px");
});
````

## Get properties 
````js
$("#circle").click(function() {
        alert($("#circle").css("background-color"));
        alert($("body").css("width"));
});
````

## Select the element that has been clicked
````js
$("div").click(function() {
        $(this).css("display", "none"); //the element that has been clicked
});
````

## Using if statement
````js
$("div").click(function() {
        if($(this).attr("id") == "circle") {
          alert("you clicked on a " + $(this).attr("id"));
        } else {
          alert("You clicked on a " + $(this).attr("class"));
        }
}); 
````

## fadeOut/fadeIn
- fadeOut
	`$(this).fadeOut("slow");`
- fadeIn
	`$(this).fadeIn("slow");`

## toggle
- Example1
````js
$("#toggle").click(function() {
            if($("#text").css("display") == "none"){
            $("#text").fadeIn();
            } else {
            $("#text").fadeOut();
            } 
});
````
- Example2
````js
      var textShowing = true;

      $("#toggle").click(function() {
        if(textShowing){
          $("#text").fadeOut(function() {
              textShowing = false;
          });
        } else {
          $("#text").fadeIn(function() {
            textShowing = true;
          });
        }
      });
````

## animate 
````js
$("#circle").click(function() {
        $(this).animate({
          width:"400px",
          height:"400px",
          marginLeft:"100px",
          marginTop:"100px",
        }, 2000, function() {
          $(this).css("background-color", "red");
        });
});
````

##AJAX: without refreshing 
skipped

## Regular expression
````js
      var regex = /is/;

      var string = "Regex is grEaT!";

      var result = string.match(regex);
      //does the 'is' appear in the string "Regex is great!"?
       alert(result);

     //대소문자 구분 없이 search하는 경우 /great/i;
     //몇번 포함되있나 알아보는경우 /e/g;
````

## Form validation 
- jquery16.html 참조
	+ .val();
	+ .show();
	+ .hide();

## jQuery-UI
````html
<script src="jquery-ui/jquery-ui.js"></script>
<link href="jquery-ui/jquery-ui.css" rel="stylesheet">
````

## More 
- Draggable
- Resizable
- Droppable
- Accordion
- Sortable
- Datepicker
- Autocomplete

## refer
- jQuery API Documentation: http://api.jquery.com
- jQuery-UI: http://jqueryui.com
- More: 
  + https://twitter.github.io/typeahead.js/
  + http://dimsemenov.com/plugins/magnific-popup/
  + http://iamceege.github.io/tooltipster/

## 끝!
이건 나의 첫 markdown문서

