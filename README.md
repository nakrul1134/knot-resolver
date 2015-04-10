# Knot DNS Resolver

[![Build Status](https://travis-ci.org/CZ-NIC/knot-resolver.svg?branch=master)](https://travis-ci.org/CZ-NIC/knot-resolver)
[![Coverage Status](https://coveralls.io/repos/CZ-NIC/knot-resolver/badge.svg)](https://coveralls.io/r/CZ-NIC/knot-resolver)
[![Coverity](https://scan.coverity.com/projects/3912/badge.svg)](https://scan.coverity.com/projects/3912)


The Knot DNS Resolver is a minimalistic caching resolver implementation. The project provides both a resolver
library and a small daemon. Modular architecture of the library keeps the core tiny and efficient, and provides
a state-machine like API for extensions. There are two built-in modules: *iterator* and *cache*,
and each module can be flipped on and off.

### Try it out?

The Knot DNS Resolver is currently in an early development phase, you shouldn't put it in the production right away.

### Docker image

This is simple and doesn't require any dependencies or system modifications, just run:

```
$ docker run cznic/knot-resolver
```

See the build page [registry.hub.docker.com/u/cznic/knot-resolver](https://registry.hub.docker.com/u/cznic/knot-resolver) for more information and options.

### Building from sources 

The Knot DNS Resolver [depends][depends] on the pre-release version of the Knot DNS library and other projects.
See the [Building project][depends] documentation page for more information.

### Running

The project builds a resolver library in the `lib` directory, and a daemon in the `daemon` directory.

```
$ ./daemon/kresolved -h
$ ./daemon/kresolved [working_directory]
```

See the documentation at [knot-resolver.readthedocs.org][doc].

[depends]: http://knot-resolver.readthedocs.org/en/latest/build.html
[doc]: http://knot-resolver.readthedocs.org/en/latest/index.html
