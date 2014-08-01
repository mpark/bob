# bob

A simple wrapper around [SCons](http://www.scons.org).

### Directory Layout

```
Projects
├─ .sconstruct
├─ src
│   └─ .sconscript
└─ out
```

### Set an Alias

```
alias bob='scons -Q --up --file=.sconstruct'
```

### Commands

__NOTE__: The `examples` directory will be used for the demo.

#### Building an Executable

`bob <path/to/name/of/binary>`

This creates the binary at the corresponding path in the `out` directory.

```
cd examples/src/c++
bob main
# The binary is at: examples/out/debug/c++/main
```

#### Build/Run a Unit Test

`bob --test <path/to/name/of/test>`

This builds and runs the unit test. Omit the `--test` to skip running the test.

```
cd examples/src/c++
bob --test foo.test
# The binary is at: examples/out/debug/c++/foo.test
```

### License

This project is licensed under the MIT License.
