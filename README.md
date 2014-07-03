# SublimeSimpleSync

Simple Sublime Text 2/3 plugin for SSH and local syncing.

## Before you start

- SSH synchronization is done via scp, your system must have SSH public-key authentication enabled.

## Installation

### Manually

Clone this project into your ST2 Packages folder, for example:

``` bash
cd [...]/Sublime Text 2/Packages
git clone https://github.com/kairyou/SublimeSimpleSync.git SimpleSync
```

### Using Package Control

Search for SimpleSync in Package Control and install it.

## Settings

When you finish installing SimpleSync, its settings can be found in Preferences > Package Settings > SimpleSync Settings

Sample settings:

``` javascript
{
  "config": {
    "autoSync": false,
    "debug": false,
    "timeout": 10
  },
  "rules": [{
    "type"     : "ssh",
    "host"     : "tnhu-ld",
    "port"     : "22",
    "username" : "tnhu",
    "password" : "password",
    "local"    : "/Users/tnhu/workspace/trunk",
    "remote"   : "/home/tnhu/workspace/trunk"
  }, {
    "type"     : "local",
    "local"    : "/Users/tnhu/Library/Application Support/Sublime Text 2/Packages/SimpleSync",
    "remote"   : "/Users/tnhu/Dropbox/projects/SimpleSync"
  }]
}
```

## Add key bindings

Preferences > Key Bindings - User

    { "keys": ["alt+s"], "command": "sublime_simple_sync"},
    { "keys": ["alt+shift+s"], "command": "sublime_simple_sync_path"},

Files are saved to remote server automatically when you save them locally. In case of "local" syncing, they are copied to "remote" folder which is on the same machine.

## Contributors

* [tnhu](https://github.com/tnhu)
* [gfreezy](https://github.com/gfreezy)
* [kairyou](https://github.com/kairyou)

* [中文文档](http://www.fantxi.com/blog/archives/sublime-simple-sync/)

## License

Copyright (c) 2009-2012 Tan Nhu

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
