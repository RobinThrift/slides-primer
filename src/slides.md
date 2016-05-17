title: Slides Primer
author: RobinThrift
twitter: RobinThrift
homepage: robinthrift.com
shortcodes: true
css:
    - 'http://fonts.googleapis.com/css?family=Droid+Sans:400,700|Source+Code+Pro|Kaushan+Script'
    - 'https://fonts.googleapis.com/css?family=Merriweather:400,700,400italic|Lato|Kaushan+Script|Source+Code+Pro'
reveal:
    controls: false
    progress: false
    slideNumber: false
    history: true
    keyboard: true
    overview: true
    transition: 'linear'
    backgroundTransition: 'slide'
    showNotes: true
    dependencies:
        - src: 'scripts/plugins/notes.js'
          async: true

-- {
    background: 
        img: '#f44f56'
}

# [var title /]

<div class="author-info">
    <h5>[var author /]</h5>
    <h5><a href="https://[var homepage /]">[var homepage /]</a></h5>
    <h5><a href="https://twitter.com/[var twitter /]">@[var twitter /]</a></h5>
</div>

--

### Outline

- this
- is
- some
- example
- text

--

```js
function extractMeta() {
    var isSlide = /(slide-*)/i,
        merge   = require('lodash.merge');
    return function(files, metalsmith, done) {
        for (var file in files) {
            if (isSlide.test(file)) {
                file = files\[file];
                // ...
            }
        }
        done();
    };
};
```

--

```scss

// AUTHOR INFO
.reveal .author-info {
    position: relative;
    bottom: -150px;
    a {
        display: block;
        font-size: inherit;
        color: inherit;
        
        &:hover {
            color: inherit;
            text-decoration: underline;
        }
    }
}
```

