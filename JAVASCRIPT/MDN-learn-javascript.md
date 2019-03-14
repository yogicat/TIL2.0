
# Learn Javascript

[https://developer.mozilla.org/en-US/docs/Learn/JavaScript/](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/)


### JS can do

- store useful values
- operations on pieces of text
- running code in response to certain events
- and more


### Javascript APIs

- APIs(Application Programming Interfaces) provide you with extra superpowers to use in your Javascript code.
- APIs are ready-made sets of code building blocks that allow a developer to implement programs.
- **Browser APIs** are built into your web browser
  - *DOM API* allows you to manipulate HTML and CSS
  - *Geolocation API* retrieves geographical information
  - *Canvas, WebGL APIs* allow you to create animated 2D, 3D graphics
  - *Audio, Video APIs* allow you to do things with multimedia
- **Third party APIs** are not built into the browser
  - *Twitter API*, *Google Maps API* , ...


## How JS works

- The browser converts HTML and CSS into the DOM
  1. Load HTML and Parse HTML -> Create DOM tree
  2. Load CSS and Parse CSS -> Attach style to DOM nodes
  3. Display the contents of the DOM
- Javascript is executed by the browser's Javascript engine (after HTML and CSS have been assembled and put together into a web page)
- Each browser tab is its own **execution environment** for running code in.

### Script loading strategies

**internal javascript**
The Javascript inside this block will not run until after the event is fired.(until the HTML body is completely loaded and parsed)

```
  document.addEventListener("DOMContentLoaded", function() {
  ...
});
```

**external javascript**
`<script src="script.js" async></script>` - `async` tells the browser to continue downloading the HTML conce the script tage elecemt has been reached.

**async**
- download the script without blocking rendering the page and will execute it as soon as the script finishes downloading.
- no guarantee that scrips will run in any specific order
- best to use when the scripts in the page run independently from each other

**defer**
- run the scrips in the order they appear in the page and execute them as soon as the scrip and content are downloaded
- best to use when scripts depend on other scripts


