# Plook
[![Build Status](http://img.shields.io/travis/injoin/plook.svg?branch=master&style=flat)](https://travis-ci.org/injoin/plook)
[![Dependency Status](http://img.shields.io/david/injoin/plook.svg?style=flat)](https://david-dm.org/injoin/plook)
[![devDependency Status](http://img.shields.io/david/dev/injoin/plook.svg?style=flat)](https://david-dm.org/injoin/plook#info=devDependencies)

Package lookup service for Bower.

## Usage
Plook is a HTTP server that does package and version lookup in the Bower registry and, if the file
is hosted in GitHub, it will print the contents of that file with the right mime type.

The requests format is the following:

```
http://<plook-server>/<package>/<version>/<file-path>
```

where:  
- `<plook-server>` is the address of a running Plook server;
- `<package>` is the name of a package registered in the Bower registry, like `jquery` or `angular`.
  The package name must be URL encoded if it contains special chars (like `/`).
- `<version>` is the targeted package version, like `1.0.0` or `v2.1.0`. The `v` prefix will be
  ignored.
- `<file-path>` is the path to the file you want to print, like `foobar.css` or `foobar/baz/qux.js`.

We have an online server running in http://plook.injoin.io so that you can use it freely with the
main Bower registry.

## License
Copyright (c) 2014 InJoin Team Licensed under the [Apache License](LICENSE).