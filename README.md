ouroboros
=========

This provides a ui spinner, a.k.a 'throbber', for modern browsers. Built with Sass, it takes 6 optional parameters.

| Parameter      | Description           | Defaults |
| ------------- |:-------------:| -----:|
| Hole color      | Color of the hole to fake a ring | transparent |
| Size      | Size of the spinner      |   46px |
| Background color light | First color, specify a lighter of the two colors      |    #ddd |
| Background color dark | Second color, specify the darker of the two colors      |    #3c76ca |
| Opacity | The opacity of the spinner      |    .8 |
| Duration | Speed of the spinner     |   3s |


## Browser Support

Works in Chrome 24+, Firefox 18+, IE 10+, Opera. A standard animated gif is provided as a fall back for older versions of IE.

## Don't Use Sass?

You can use the CSS that the Sass generates in `stylesheets/main.scss` and make edits to the parameters described above.