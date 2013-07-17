# -prefix-LESS
A mixin for add prefixes in less with unlimited arguments.

## Live Demo
You can see the mixin running on <a href="http://codepen.io/ivanbanov/pen/tHlfh" target="_blank">codepen</a>.

## Usage
```
.prefix(property, val, prefixes)
```

Any value that need whitespace is necessary use as string to prevent errors.

__NOTE__: Less dont accept string as property then is need use a additional trick with a fake property
lessfix: property;

For more information see this issue <a href="http://codepen.io/ivanbanov/pen/tHlfh" target="_blank">#698</a> in official github of LESS.

## Outputs
__Single value__
```
.prefix(box-sizing, border-box, 'webkit moz');

lessfix: box-sizing;
-webkit-box-sizing: border-box;
-moz-box-sizing: border-box;
box-sizing: border-box;
```

__Multiple value__
```
.prefix(box-shadow, '4px 5px 10px #049cdb, 10px 10px 10px #ffc40d, 15px 15px 10px #46a546', webkit);

lessfix: box-shadow;
-webkit-box-shadow: 4px 5px 10px #049cdb, 10px 10px 10px #ffc40d, 15px 15px 10px #46a546;
box-shadow: 4px 5px 10px #049cdb, 10px 10px 10px #ffc40d, 15px 15px 10px #46a546;
```
