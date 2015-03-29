# Coffee Waterfall

Waterfall in coffee. Compatibility: IE9+

### Build

```shell
coffee -c waterfall.coffee
```

### How to use

```javascript
var waterfall = new Waterfall({ container: '', box: '' });

window.onresize = function() {
    if(clr) clearTimeout(clr);
    clr = setTimeout(function() {
        waterfall.compose();
    }, 500);
};
```

Tell constructor how to select the container and the boxes in it. Default container is `.wf-container`, and default box is `.wf-box`. It use `querySelector/querySelectorAll` inside. Then constructor will do composing once. Then you can invoke `waterfall.compose()` when you need to compose the boxes again.
