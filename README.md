# rc-exports-loader
A webpack loader for babel-style rc files

## Usage

Given a file such as:

```
#.testrc
{
    plugins: [
        'foo'
    ]
}
```

This will transform the file to export the object for usage in `import` statements

```javascript
import test from './testrc';

test.plugins; // [ 'foo' ]

```

## Config

Basic `webpack.config.js` syntax applies:

```

module: {
    rules: [
        {
            test: /\.testrc$/,
            use: 'rc-exports-loader'
        }
    ]    
}

```

