# pretty-imperial [![Build Status](https://travis-ci.org/stevelacy/pretty-imperial.svg?branch=master)](https://travis-ci.org/stevelacy/pretty-imperial)

> Parse, convert, and humanize imperial sizes

## Install

```shell
$ npm install pretty-imperial
```
## Usage

```js

const prettyImperial = require('pretty-imperial')

prettyImperial(15000).humanize()
// => 2.84mi

prettyImperial(.5).humanize()
// => 6in

// Using input types
prettyImperial(120).input('in').humanize()
// => 10ft

```

## Functions

#### .mi(), .ft(), .in()
> Converts the input measurement to the corresponding output

Default input measurement type is `foot`. It can be changed with `.input()`

```js
prettyImperial(1).in()
// => 0.12ft
```

#### humanize()
> Converts the input value to a more human recognizable size

```js
prettyImperial(120).humanize()
// => 120ft

```

#### input()
> Sets the input value to a particular imperial type

This can be chained with `humanize()`

```js
prettyImperial(1500).input('in').ft()
// => 125ft

```

## Supported sizes

```
mi: mile  - 5280ft
ft: foot - 12in
in: inch - 1/12ft

```

## [License](LICENSE) (MIT)
