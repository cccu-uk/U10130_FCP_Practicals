# Syntax Highlighting

mdBook uses [Highlight.js](https://highlightjs.org) with a custom theme for syntax highlighting.

Automatic language detection has been turned off, so you will probably want tospecify the programming language you use like this:

~~~markdown
```rust
fn main() {
    // Some code
}
```
~~~
Output:
```rust
fn main() {
    // Some code
}
```
or ...
~~~markdown
```bash
main(){

}
```
~~~
Output:
```bash
main(){

}
```
## Supported languages

These languages are supported by default:

- apache
- armasm
- bash
- c
- coffeescript
- cpp
- csharp
- css
- d
- diff
- go
- handlebars
- haskell
- http
- ini
- java
- javascript
- json
- julia
- kotlin
- less
- lua
- makefile
- markdown
- nginx
- objectivec
- perl
- php
- plaintext
- properties
- python
- r
- ruby
- rust
- scala
- scss
- shell
- sql
- swift
- typescript
- x86asm
- xml
- yaml