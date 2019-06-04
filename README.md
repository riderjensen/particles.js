# particles.js

particles.js is a lightweight, dependency-free and responsive javascript plugin for particle backgrounds.

[Original Repo](https://github.com/marcbruederlin/particles.js/archive/master.zip)


## Usage

Add a canvas element to your markup (it should be the last element)
```html
<body>
  <style>
    html,
    body {
      margin: 0;
      padding: 0;
    }

    .background {
      position: absolute;
      display: block;
      top: 0;
      left: 0;
      z-index: 0;
    }
  </style>
  <canvas class="background"></canvas>
  <script src="path/to/particles.min.js"></script>
  <script>
    window.onload = function() {
      Particles.init({
        selector: '.background'
      });
    };
  </script>
</body>
```

## Options
Option | Type | Default | Description
------ | ------------- | ------------- | -----------
`selector` | string | - | *Required:* The CSS selector of your canvas element
`maxParticles` | integer | `100` | *Optional:* Maximum amount of particles
`sizeVariations` | integer | `3` | *Optional:* Amount of size variations
`speed` | integer | `0.5` | *Optional:* Movement speed of the particles
`color` | string or string[] | `#000000` | *Optional:* Color(s) of the particles and connecting lines
`minDistance` | integer | `120` | *Optional:* Distance in `px` for connecting lines
`connectParticles` | boolean | `false` | *Optional:* `true`/`false` if connecting lines should be drawn or not
`responsive` | array | `null` | *Optional:* Array of objects containing breakpoints and options
`shape` | array | `sqr` | *Optional:* Array of objects containing draw commands amd coordinates

Example how to use the [responsive option](https://marcbruederlin.github.io/particles.js/#responsive-option).

Example how to use the [shape option](https://github.com/riderjensen/particles.js/blob/master/test/index.html).

## Methods
Method | Description
------ | -----------
`pauseAnimation` | Pauses/stops the particle animation
`resumeAnimation` | Continues the particle animation
`destroy` | Destroys the plugin

Example how to use the [public methods](https://marcbruederlin.github.io/particles.js/#use-methods).

## Browser Support
IE9+ and all modern browsers.

## Examples
See [various examples](https://marcbruederlin.github.io/particles.js/#examples) how you can use particles.js.

## Build
To compile the distribution files by yourself, make sure that you have node.js and gulp installed, then:
- Clone the repository: `https://github.com/marcbruederlin/particles.js.git`
- Change in the project directory: `cd particles.js`
- Install the dependencies: `npm install`
- Run the gulp build task `gulp build` to regenerate the `dist` folder. <br/> You can also run `gulp build --watch` to watch for file changes and automatically rebuild the files.


