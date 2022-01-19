# How to use SVG
Explanation about how SVG can be used in an page

## SVG as image
SVG can be used in an HTML page with the ``` <img/> ``` tag.
```
<img src="./img/alarm_clock.svg" alt="Clock">
```
### Advantages and disadvantages of the SVG as ``` <img/> ```
* They can be cached :)
* No interation with CSS :(
* No interation at DOM :(
* Animations only work if they're in the SVG file (don't work if we would make then with JS, for example) :(

## SVG as background
SVG also can be used as background image in any HTML element
```
  <style>
    .icon-music{
      background-image: url('./img/audio_file.svg')
    }
  </style>
```
### Advantages and disadvantages of the SVG as ``` background-image ```
* Can be cached :)
* No CSS interation :(
* No DOM interation :(
* Animations only works if they're inside of the SVG file :(
* Comparing with the previous case, it has a little advantage that we can select the src in the CSS HTML selector so it doesn't have to load the image if the HTML element doesn't have the specific class :)

## SVG as iframe/object/embed
```
<iframe src="./../assets/img/alarm_clock.svg" frameborder="0"></iframe>
```
```
<object data="./../assets/img/alarm_clock.svg" type=""></object>
```
```
<embed src="./../assets/img/alarm_clock.svg" type="">
```

### Advantages and disadvantages of the SVG as ``` <iframe/> / <object/> /<embed/>```
* Slow rendering :(
* Differents behaviors depending on the browser :(
* Don't allow so many editions :(

## SVG as data-uri
In that case, whe can use both as image or as background-image

### SVG as data-uri in ``` background-image ```
```
<style>
    .icon-clock{
      height: 100px;
      width: 100px;
      background-image: url(data:image/svg+xml;base64,PHN2ZyB2ZXJzaW9uPSIxIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA0OCA0OCIgZW5hYmxlLWJhY2tncm91bmQ9Im5ldyAwIDAgNDggNDgiPgogICAgPGcgZmlsbD0iIzM3NDc0RiI+CiAgICAgICAgPHBhdGggZD0iTTM4LjUsNDQuNmwtNC00bDIuMS0yLjFsNCw0YzAuNiwwLjYsMC42LDEuNSwwLDIuMWwwLDBDNDAuMSw0NS4xLDM5LjEsNDUuMSwzOC41LDQ0LjZ6Ii);
    }
  </style>
``` 
### SVG as data-uri in ```` <img/> ````
```
<img src="data:image/svg+xml;base64,PHN2ZyB2ZXJzaW9uPSIxIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA0OCA0OCIgZW5hYmxlLWJhY2tncm91bmQ9Im5ldyAwIDAgNDggNDgiPgogICAgPGcgZmlsbD0iIzM3NDc0RiI+CiAgICAgICAgPHBhdGggZD0iTTM4LjUsNDQuNmwtNC00bDIuMS0yLjFsNCw0YzAuNiwwLjYsMC42LDEuNSwwLDIuMWwwLDBDNDAuMSw0NS4xLDM5LjEsNDUuMSwzOC41LDQ0LjZ6Ii" alt="Clock"/>
```

### Advantages and disadvantages of the SVG as ``` data-uri ``` 
* They're not cached :(
* No CSS interaction :(
* No DOM interaction :(
* The size of the data-uri sometimes can be bigger than the SVG code :(

## SVG inline
This type represents the self SVG code inside the HTML file.
```
<body>
  <h1>SVG inline</h1>

  <svg version="1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 48 48" enable-background="new 0 0 48 48">
    <g fill="#37474F">
        <path d="M38.5,44.6l-4-4l2.1-2.1l4,4c0.6,0.6,0.6,1.5,0,2.1l0,0C40.1,45.1,39.1,45.1,38.5,44.6z"/>
        <path d="M9.5,44.6l4-4l-2.1-2.1l-4,4c-0.6,0.6-0.6,1.5,0,2.1l0,0C7.9,45.1,8.9,45.1,9.5,44.6z"/>
    </g>
    <circle fill="#C62828" cx="24" cy="24" r="20"/>
    <circle fill="#eee" cx="24" cy="24" r="16"/>
    <rect x="19" y="22.1" transform="matrix(-.707 -.707 .707 -.707 12.904 62.537)" fill="#E53935" width=".8" height="13"/>
    <rect x="23" y="11" width="2" height="13"/>
    <rect x="26.1" y="22.7" transform="matrix(-.707 .707 -.707 -.707 65.787 27.25)" width="2.3" height="9.2"/>
    <circle cx="24" cy="24" r="2"/>
    <circle fill="#C62828" cx="24" cy="24" r="1"/>
    <rect x="22" y="1" fill="#37474F" width="4" height="3"/>
    <g fill="#37474F">
        <path d="M44.4,16.2c2.5-3.5,2.1-8.4-1-11.5c-3.1-3.1-8-3.5-11.5-1L44.4,16.2z"/>
        <path d="M3.6,16.2c-2.5-3.5-2.1-8.4,1-11.5c3.1-3.1,8-3.5,11.5-1L3.6,16.2z"/>
    </g>
  </svg>

</body>
</html>
```
### Advantages and disadvantages of the SVG as ```<svg>```
* Images can't be cached
* Allow DOM interaction
* Allow CSS animations and interactions
* No needed HTTP additional requests
