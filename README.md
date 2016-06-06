# img-slider

`<img-slider>` is an element that provides an easy to use images slider fed by an array of urls that
points to images. This array of urls can be changed programatically and `<img-slider>` will take care of all the
changes needed.

`<img-slider>` can be fed both **declaratively** and **imperatively** through it's property `imgUrlArray`.

Example:

<img-slider img-url-array='["/url1", "/url2"]'></img-slider>

> Note the use of the single and double quotes. You have to respect the structure in order to the element to work

```
var element = document.querySelector('img-slider');
element.imgUrlArray = ["/url1", "/url2"];
```


By default the slides doesn't change automatically, but the user can set a timer interval through the attribute
`interval`. `interval` receives the number of milliseconds the user wants for the timer.

Example:

<img-slider img-url-array="['/url1', '/url2']"
            interval="2000"></img-slider>


The UI for change images manually are a couple of pads at both sides of the image to change forward and backwards.
Besides, for giving some feedback to the user about the number of the images in the slider, there's a bullet navigation
panel at the bottom of the slider (And those buttons can be pressed as well for navigation).

The size of the slider can be set by using the attributes `width` and `height`

## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install

## Install img-slider

For installing the component just run on you CLI

```
bower install --save https://github.com/edgarshurtado/img-slider.git
```


## Playing With img-slider

If you wish to work on `img-slider` in isolation, I recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polyserve

And you can run it via:

    polyserve

Once running, you can preview your element at
`http://localhost:8080/components/seed-element/`, where `seed-element` is the name of the directory containing it.


## Testing img-slider

Simply navigate to the `/test` directory of your element to run its tests. If
you are using Polyserve: `http://localhost:8080/components/seed-element/test/`

### web-component-tester

The tests are compatible with [web-component-tester](https://github.com/Polymer/web-component-tester).
Install it via:

    npm install -g web-component-tester

Then, you can run your tests on _all_ of your local browsers via:

    wct

#### WCT Tips

`wct -l chrome` will only run tests in chrome.

`wct -p` will keep the browsers alive after test runs (refresh to re-run).

`wct test/some-file.html` will test only the files you specify.

