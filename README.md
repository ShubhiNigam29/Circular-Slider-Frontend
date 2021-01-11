# Objective

Create reusable circular slider class in javascript (as shown in image below). Make sure to
optimize the code for mobile performance.

# Notes
● when creating new instance of the slider, pass in the options object <br />
● multiple sliders can be rendered in the same container (see image below) <br />
● each slider should have his own max/min limit and step value <br />
● value number (on the left in the image) should change in real time based on the slider’s
position <br />
● make sure touch events on one slider don’t affect others (even if finger goes out of
touched slider range) <br />
● slider value should change when you drag the handle or if you tap the spot on a slider <br />
● the solution should work on mobile devices <br />
● without the use of any external JS libraries <br />
● use GitHub to source your code (make sure you commit early and often) <br />

# Options
● container <br />
● color <br />
● max/min value <br />
● step <br />
● radius <br />

![alt text](https://github.com/ShubhiNigam29/Circular-Slider-Frontend/blob/main/sliders.png)

# Solution

Created a slider using vanilla JS. It's reusable, and customizable.

## Live Demo

[a link](https://raw.githack.com/ShubhiNigam29/Circular-Slider-Frontend/main/index.html)

## Steps

1. "Option" object is defined <br />

```
const Options = {
    DOMselector: string,
    sliders: [
      {
        radius: number,
        min: number,
        max: number,
        step: number,
        initialValue: number,
        color: string,
        displayName: string
      }
    ]
};

```

2. Option description <br />

- selector -> container selector <br />
- sliders -> array of options objects for sliders <br />
- radius -> radius of the slider <br />
- min -> minimum value of the slider <br />
- max -> maximum value of the slider <br />
- step -> value step <br />
- initialValue -> value of the slider on initialization <br />
- color -> color of the slider (valid hex code value) <br />
- displayName -> name of the item <br />

3. Create instance of Slider class and call draw() method: <br />

```
const slider = new Slider(Options);
slider.draw();

```

The slider is now ready to use!