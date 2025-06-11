# Programming Languages on Termux 

## ![Arturo](https://skillicons.dev/icons?i=arturo) Arturo

### Compiler

```sh
pkg i arturo
```


## ![C/C++](https://skillicons.dev/icons?i=c,cpp) C/C++

### Compiler

```sh
pkg i clang
```


## ![Clojure](https://skillicons.dev/icons?i=clojure) Clojure

### Compiler

https://clojure.org/guides/install_clojure#_linux_instructions

### Formatter

- cljfmt

https://github.com/weavejester/cljfmt/releases/download/${version}/cljfmt-${version}-linux-aarch64.tar.gz

```sh
# glibc-runner patch
grun -c cljfmt

# move to ~/.local/bin
mv cljfmt ~/.local/bin/cljfmt-glibc

# create executable shell
cat <<EOF > ~/.local/bin/cljfmt
#!/data/data/com.termux/files/usr/bin/env bash
grun -s "cljfmt-glibc $@"
EOF
chmod +x ~/.local/bin/cljfmt
```

### LSP

- clojure-lsp

https://github.com/clojure-lsp/clojure-lsp/releases/download/${version}/clojure-lsp-native-linux-aarch64.zip

```sh
# glibc-runner patch
grun -c clojure-lsp

# move to ~/.local/bin
mv clojure-lsp ~/.local/bin/clojure-lsp-glibc

# create executable shell
cat <<EOF > ~/.local/bin/clojure-lsp
#!/data/data/com.termux/files/usr/bin/env bash
grun -s "clojure-lsp-glibc -Djava.io.tmpdir=$TMPDIR $@"
EOF
chmod +x ~/.local/bin/clojure-lsp
```

## ![Crystal](https://skillicons.dev/icons?i=crystal) Crystal

### Compiler / Formatter

```sh
pkg i crystal
```

## ![Dart](https://skillicons.dev/icons?i=dart) Dart

### Compiler / Formatter / LSP

```sh
pkg i dart
```

## ![Elixir](https://skillicons.dev/icons?i=elixir) Elixir

### Compiler / Formatter

```sh
pkg i elixir

export PATH=~/.cache/rebar3/bin:$PATH
export MIX_OS_CONCURRENCY_LOCK=0
```

## ![Erlang](https://skillicons.dev/icons?i=erlang) Erlang

### Compiler
```sh
pkg i erlang
```

## ![Fennel](https://skillicons.dev/icons?i=fennel) Fennel

### Compiler

```sh
pkg i fennel
```

### Formatter

- fnlfmt

https://git.sr.ht/~technomancy/fnlfmt

### LSP

- fennel-ls

https://git.sr.ht/~xerool/fennel-ls/tree/HEAD/docs/installation.md

## ![Flix](https://skillicons.dev/icons?i=flix) Flix

### Compiler / LSP

https://github.com/flix/flix/releases/download/v${version}/flix.jar

```sh
# move to ~/.local/lib/flix/
mkdir ~/.local/lib/flix 
mv flix.jar ~/.local/lib/flix/

# create executable shell
cat <<EOF > ~/.local/bin/flix
#!/usr/bin/env bash
java -jar ~/.local/lib/flix/flix.jar "$@"
EOF
chmod +x ~/.local/bin/flix
```


## ![Gleam](https://skillicons.dev/icons?i=gleam) Gleam

### Compiler / Formatter / LSP

```sh
pkg i gleam
```


## ![Go](https://skillicons.dev/icons?i=go) Go

### Compiler / Formatter

```sh
pkg i golang

export PATH=~/go/bin:$PATH
```

### LSP

```sh
pkg i gopls
```

## ![Janet](https://skillicons.dev/icons?i=janet) Janet

### Compiler

https://github.com/janet-lang/janet?tab=readme-ov-file#macos-and-unix-like

OR 

```sh
pkg i janet
```

### Formatter

- janet-format

https://github.com/janet-lang/spork?tab=readme-ov-file#build

```sh
export PATH=~/../usr/lib/janet/bin:$PATH
```

## ![Java](https://skillicons.dev/icons?i=java) Java (not GraalVM NativeImage)

### Compiler

```sh
pkg i openjdk-21
```

## ![JavaScript / TypeScript](https://skillicons.dev/icons?i=javascript,typescript) JavaScript / TypeScript

### Compiler

```sh
pkg i nodejs
```

## ![LFE](https://skillicons.dev/icons?i=lfe) LFE

### Compiler

https://cnbbooks.github.io/lfe-tutorial/introduction/install.html

## ![Lua](https://skillicons.dev/icons?i=lua) Lua

### Compiler

```sh
pkg i lua53
```

### Formatter

- stylua

```sh
pkg i stylua
```

### LSP

- lua-language-server

```sh
pkg i lua-language-server
```

## ![Nim](https://skillicons.dev/icons?i=nim) Nim

### Compiler

```sh
pkg i nim

export PATH=~/.nimble/bin:$PATH
```

### Formatter

- nph

```sh
nimble install nph
```

### LSP

- nimlangserver

```sh
nimble install nimlangserver
```

## ![Perl](https://skillicons.dev/icons?i=perl) Perl

### Compiler

```sh
pkg i perl
```

## ![Python](https://skillicons.dev/icons?i=python) Python

### Compiler

```sh
pkg i python3
```

### Formatter / LSP

- ruff

```
pkg i ruff
```

## ![Racket](https://skillicons.dev/icons?i=racket) Racket

### Compiler

```sh
pkg i racket
```

### Formatter

```sh
raco pkg install fmt
```


## ![Raku](https://skillicons.dev/icons?i=raku) Raku

### Compiler

```sh
pkg i rakudo
```


## ![Rust](https://skillicons.dev/icons?i=rust) Rust

### Compiler / Formatter

```sh
pkg i rust
```

### LSP

```sh
pkg i rust-analyzer
```

## ![Swift](https://skillicons.dev/icons?i=swift) Swift

### Compiler / Formatter

```sh
pkg i swift
```

### LSP

```sh
pkg i sourcekit-lsp
```


## ![Zig](https://skillicons.dev/icons?i=zig) Zig (requires Linux Kernel at least v3.16)

### Compiler / Formatter

```sh
pkg i zig
```

### LSP

```sh
pkg i zls
```

