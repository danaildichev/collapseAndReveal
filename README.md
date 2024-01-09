# collapseAndReveal

![Static Badge](https://img.shields.io/badge/version-1-blue)

Slide a content block's height up or down.

Use the class in, `slide.js` to control how an element's height is animated. Accompanying HTML and CSS can be found in the `index.html` file. Styling options can be scale, fade, or both. Height animations can be synchronous with styling or staggered.

## Live Demo

[https://danaildichev.net/portfolio/code-samples/collapse-and-reveal](https://danaildichev.net/portfolio/code-samples/collapse-and-reveal)

## Install

Get a copy of `slide.js` and initialize an instance

```javascript
<script src="/path/to/slide.js"></script>

<script>

    /**
     * @param {string} checkID checkbox for toggling
     * @param {string} slideID the content container to be toggled
     * @param {string} animationType "scale", "fade", or "both"
     * @param {number} durationUp milliseconds for slide up animation
     * @param {boolean} staggerUp if display/height animation are out of sync
     * @param {number} durationDown milliseconds for slide down animation
     * @param {boolean} staggerDown if height/display animation are out of sync
     * @param {string} heightClass css for sled max height
     * @param {string} iconID the icon to be toggled after sliding
     * @param {number} iconDelayUp milliseconds offset for icon animation
     * @param {number} iconDelayDown milliseconds offset for icon animation
     */
    const slideDemo = new Slide(checkID, slideID, animationType, durationUp, staggerUp, durationDown, staggerDown, heightClass, iconID, iconDelayUp, iconDelayDown);

</script>
```

## Usage

You will need a button to trigger the animation, a checkbox for keeping track of state, and a container to be animated. Animations and styles are handled with a handful of custom CSS. See the demo file for more details. The demo also makes use of Tailwind, Daisy UI, Font Awesome.

```HTML
<!-- button: toggle slide -->
<button id="btn-slideDemo" onclick="slideDemo.toggleSlide()">
    <i id="icon-slideDemo"></i>
    Toggle
</button>


<!-- checkbox for slide toggle -->
<input type="checkbox" id="checkbox-slideDemo" checked>


<!-- example container -->
<div id="container-slideDemo">

    <!-- content -->
    <p>EXAMPLE CONTENT BLOCK</p>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>

</div>
<!-- end example container -->
```

## API

The `Slide` class does not expose any functions or options other than the three arguments passed in at the time of construction.

## Issues

Open an issue or hit me up.

## Contributing

PRs accepted.

## License

GPL-3.0
