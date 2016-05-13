# img-slider

`<img-slider>` is an element that provides an easy to use images slider fed by an array of urls that
points to images.

`<img-slider>` can be fed both **declaratively** and **imperatively** through it's property `imgUrlArray`.

Example:
```html
    <img-slider img-url-array="['/url1', '/url2']"></img-slider>
```

```javascript
var element = document.querySelector('img-slider');
element.imgUrlArray = ["/url1", "/url2"];
```

By default the slides doesn't change automatically, but the user can set a timer interval through the attribute
`interval`. `interval` receives the number of milliseconds the user wants for the timer.

Example:

```html
    <img-slider img-url-array="['/url1', '/url2']"
                interval="2000"></img-slider>
```

The size of the slider can be set by using the attributes `width` and `height`

## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install


## Playing With img-slider

If you wish to work on `img-slider` in isolation, we recommend that you use
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

