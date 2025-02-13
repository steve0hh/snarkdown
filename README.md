<p align="center">
  <img src="https://cdn.jsdelivr.net/emojione/assets/svg/1f63c.svg" width="256" height="256" alt="Snarkdown">
  <br>
  <a href="https://www.npmjs.org/package/snarkdown"><img src="https://img.shields.io/npm/v/snarkdown.svg?style=flat" alt="npm"></a> <a href="https://travis-ci.org/developit/snarkdown"><img src="https://travis-ci.org/developit/snarkdown.svg?branch=master" alt="travis"></a>
</p>


Snarkdown is a dead simple **1kb** [Markdown] parser.

It's designed to be as minimal as possible, for constrained use-cases where a full Markdown parser would be inappropriate.

This fork of [snarkdown](https://github.com/developit/snarkdown) encompasses of customization for my use cases.

## Customization

These are a list of customizations that I've done:

**Opens links with new tabs**

```javascript
> snarkdown('[Snarkdown::newtab](http://github.com/steve0hh/snarkdown)'))
<- <a href="http://github.com/steve0hh/snarkdown" target="_blank">Snarkdown</a>'
```

## Features

- **Fast:** since it's basically one regex and a huge if statement
- **Tiny:** it's 1kb of gzipped ES3
- **Simple:** pass a Markdown string, get back an HTML string

> **Note:** Tables are not yet supported. If you love impossible to read regular expressions, submit a PR!

## Demos & Examples

- ⚛️ [**Snarky**](https://snarky.surge.sh) - markdown editor built with Preact & Snarkdown
- ✏️ [**Simple Markdown Editor**](http://jsfiddle.net/developit/828w6t1x/)


## Usage

Snarkdown exports a single function, which parses a string of Markdown and returns a String of HTML. Couldn't be simpler.

The snarkdown module is available in [every module format](https://unpkg.com/snarkdown/dist/) you'd ever need: ES Modules, CommonJS, UMD...

```js
import snarkdown from 'snarkdown';

let md = '_this_ is **easy** to `use`.';
let html = snarkdown(md);
console.log(html);
// <em>this</em> is <strong>easy</strong> to <code>use</code>.
```


## License

MIT


[Markdown]: http://daringfireball.net/projects/markdown/
