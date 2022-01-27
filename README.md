# SVG Structure
SVG files have a specific structure

## Cartesian Plane
To understand SVG is important to know how the cartesian plane works.

![Cartesian plane with some spots](./assets/img/cartesian-plane.png)

## ViewPort and ViewBox
The <strong>viewport</strong> is the space defined by the ```<svg>``` tag. Things that are outside of that, won't appear in the visualization.
```
<svg width="300px" height="100px" style="border:2px solid red; margin:0 auto; display:block;">
  <circle r="25" cx="0" cy="0"/>
</svg>
```
Above, for example, part of the circle stays outside of the port defined by the ```<svg>``` tag:

![Viewport](./assets/img/viewport.png)

The <strong>viewbox</strong>, in its turn, is a property of the ````<svg>``` tag. ViewBox receive 4 values that, in order, represents:
* X axes (viewport movement in the X axes)
* Y axes (viewport movement in the Y axes)
* X proportion
* Y proportion

Summarizing, the ```viewBox``` determines the proportion of the viewPort size in the coordenates. It's as the resolution of the viewPort (zoom-in/out)
```
<svg width="300px" height="100px" viewBox="0 0 600 200" style="border:2px solid red; margin:0 auto; display:block;">
  <circle r="25" cx="150" cy="50"/>
</svg>
```
![ViewBox](./assets/img/viewbox.png)
Now, decreasing the proportion of X and Y, but without moving on the coordinates and circle size, we will have this:
```
<svg width="300px" height="100px" viewBox="0 0 150 50" style="border:2px solid red; margin:0 auto; display:block;">
  <circle r="25" cx="150" cy="50"/>
</svg>
```
![ViewBox](./assets/img/viewbox2.png)

## preserveAspectRatio
Defines the behavior of the dimensions or of the image when the viewport changes.
```
<svg
    width="230" height="218"
    viewBox="0 0 230 218"
    preserveAspectRadio="">
</svg>
```
There are some values accepted:
* "none" = the image won't preserve its form if some dimension change.
* "< 1st value > < 2nd value >"
  * the 1st value is about the align of the image i the X and Y axes, alternating between Min, Mid and Max.
    *xMinYMin
    *xMidYMin
    *xMaxYMin
  * the 2nd value can be:
    * meet (cover the max the image can, without distortion)
    * slice (cut the image if it pass the viewport). The cut is done in the smallest measure according to the image proportion.

