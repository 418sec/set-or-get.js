[![set-or-get](http://i.imgur.com/EsztPQ4.png)](#)

# set-or-get [![PayPal](https://img.shields.io/badge/%24-paypal-f39c12.svg)][paypal-donations] [![Version](https://img.shields.io/npm/v/set-or-get.svg)](https://www.npmjs.com/package/set-or-get) [![Downloads](https://img.shields.io/npm/dt/set-or-get.svg)](https://www.npmjs.com/package/set-or-get) [![Get help on Codementor](https://cdn.codementor.io/badges/get_help_github.svg)](https://www.codementor.io/johnnyb?utm_source=github&utm_medium=button&utm_term=johnnyb&utm_campaign=github)

> Sets or gets an object field value.

## Installation

```sh
$ npm i --save set-or-get
```

## Example

```js
// Dependencies
var SetOrGet = require("set-or-get");

// Create an object
var cache = {};

SetOrGet(cache, "foo", []).push(42);
// { foo: [42] }

SetOrGet(cache, "bar", {}).baz = 42;
// { foo: [42], bar: { baz: 42 } }

SetOrGet(cache, "foo", []).push(7);
// { foo: [42, 7], bar: { baz: 42 } }

console.log(cache);
// =>
// {
//   foo: [42, 7]
// , bar: { baz: 42 }
// }
```

## Documentation

### `SetOrGet(input, field, def)`
Sets or gets an object field value.

#### Params
- **Object|Array** `input`: The cache/input object.
- **String|Number** `field`: The field you want to update/create.
- **Object|Array** `def`: The default value.

#### Return
- **Object|Array** The field value.

## How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].

## Where is this library used?
If you are using this library in one of your projects, add it in this list. :sparkles:

 - [`count-words`](https://github.com/IonicaBizau/count-words#readme)

 - [`engine-parser`](https://github.com/IonicaBizau/engine-parser) by jillix

 - [`enny`](https://github.com/IonicaBizau/enny) by jillix

 - [`lien`](https://github.com/LienJS/Lien)

 - [`svg.connectable.js`](https://github.com/jillix/svg.connectable.js) by jillix

## License

[MIT][license] © [Ionică Bizău][website]

[paypal-donations]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=RVXDDLKKLQRJW
[donate-now]: http://i.imgur.com/6cMbHOC.png

[license]: http://showalicense.com/?fullname=Ionic%C4%83%20Biz%C4%83u%20%3Cbizauionica%40gmail.com%3E%20(http%3A%2F%2Fionicabizau.net)&year=2015#license-mit
[website]: http://ionicabizau.net
[contributing]: /CONTRIBUTING.md
[docs]: /DOCUMENTATION.md