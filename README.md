# actual-empty-object

I am using this to shim modules in a react-native project but this can also be used with browserify.
It does what is says on the tin, it exports an empty object, thats it!
Compatibility goes way back to the first node version, and it's 100% bug free.

## Install

```js
npm install --save actual-empty-object
```

## Use

Let's replace the fs module with an empty object in a browserify build

```json
"browser": {
  "fs": "actual-empty-object"
}
```

Using the "react-native" (or the browser) field in a react-native project to shim the fs module didn't work for me.

For the time being, I am now resorting to a rather hacky:

```shell
mkdir node_modules/fs && echo 'module.exports = {};' > node_modules/fs/index.js
```

## License

MIT
