*This repository is a mirror of the [component](http://component.io) module [component/t](http://github.com/component/t). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/component-t`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# t

  tiny translation helper.

## Installation

    $ component install component/t

## API

### t(string, [object], [lang])

  Return a translatable `string`, with optional
  substitutions keyed in `object` using language `lang`.

```js
var t = require('t');

t('Hello');
// => "Hello"

t('Hello {name}', { name: 'Tobi' });
// => "Hello Tobi"
```

### t.lang()

  Get the current language code, for example "en".

### t.lang(code)

  Set language `code`.

### t.CODE = object

  Define translations, for example:

```js
t.es = {
  'Hello {name}': 'Hola {name}'
};

t('Hello {name}', { name: 'Tobi' });
// => "Hello Tobi"

t.lang('es');
t('Hello {name}', { name: 'Tobi' }).should.equal('Hola Tobi');
// => "Hola Tobi"
```

# License

  MIT

