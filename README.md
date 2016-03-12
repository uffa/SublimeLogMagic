# SublimeLogMagic

Easily log javascript variables and parameters with keyboard shortcut.


## Installing

Clone this repository into your Packages directory (Package Control support coming soon).

## Usage

Simply press `cmd+alt+j` (`ctrl+alt+j`) to produce magic downwards or `cmd+alt+k` (`ctrl+alt+k`) to produce magic upwards.

You can also run these commands manually:
- `LogMagic Statement (down)`
- `LogMagic Statement (up)`

## Features

### Log quickly

Any log statement is just a keyboard shortuct away

### Log anything

LogMagic inspects the current line and tries to extract interesting information from it:
- variable assignments
- function parameters in a function definition
- parameters in case of a function call
- supports ES6 destructuring
- supports ES6 optional parameters
- supports flowtype (to some extent)
- falls back to printing `L#` where `#` is the line number if it fails

![Log anything quickly](https://github.com/syko/SublimeLogMagic/raw/master/src/images/log-anything.gif "Log anything quickly")

### Cycle through log types

Press the same keyboard shortcuts when on already on a log statement to cycle through `log`,
`info`, `warn` and `error` types.

![Log cycle](https://github.com/syko/SublimeLogMagic/raw/master/src/images/log-anything.gif "Cycling through log levels is a breeze")

### Up / Down support

You can add the log statement on the previous line or the next line. This is helpful in case of return
statements for example.

![Log upwards](https://github.com/syko/SublimeLogMagic/raw/master/src/images/log-up.gif "Log upwards!")

This can also change what's logged. Eg in the following case we're more interest in the
arguments passed to the callback than the value of the variable.

![Log upwards smartly](https://github.com/syko/SublimeLogMagic/raw/master/src/images/log-up-change.gif "Logging upwards changes everything!")

### ES6 destructuring support

LogMagic can parse destructuring and extract the necessary variable names from it (even
in case of renamed properties)

![Log ES6 destructuring](https://github.com/syko/SublimeLogMagic/raw/master/src/images/log-destruct.gif "Supports ES6 Destructuring parameters")

### Flowtype support

Flowtype is cool. Best effort has been made to ignore flowtype's annotations and still produce a meaningful
log statement (but expect kinks and bugs here).

![Log with Flowtype](https://github.com/syko/SublimeLogMagic/raw/master/src/images/log-flowtype.gif "Supports some flowtype")