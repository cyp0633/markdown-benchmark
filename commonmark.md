**Most of the content is from [CommonMark Spec 0.30](https://spec.commonmark.org/0.30/#preliminaries). Licenced with CC BY-SA 3.0**

# 2 Preliminaries

## Characters and lines

苟利国家生死以，岂因祸福避趋之。😂

## Tabs

    foo bar

> a code block

>       foo

> a code block quote

## Backslash escapes

\!\"\#\$\%\&\'\(\)\*\+\,\-\.\/\:\;\<\=\>\?\@\[\\\]\^\_\`\{\|\}\~

> All of them should be escaped

\*not emphasized*
\<br/> not a tag
\[not a link](/foo)
\`not code`
1\. not a list
\* not a list
\# not a heading
\[foo]: /url "not a reference"
\&ouml; not a character entity

> as said above

## Entity and numeric character 

&nbsp; &amp; &copy; &AElig; &Dcaron;
&frac34; &HilbertSpace; &DifferentialD;
&ClockwiseContourIntegral; &ngE;

> some entity references

# Leaf blocks

***
---
___

> Three indentation lines

 **  * ** * ** * **

   _____

> Also right

    ***
__

    ___

> Not right

## ATX headings

# H1

## H2

### H3

#### H4

##### H5

###### H6

> H1 to H6

####### H7

> Not a heading

#5 bolt

#hashtag

> Not allowed

## Setext headings

H1
and another line
======

H2 *and
italic text*
   ------

> As said above
> 
> Note: Some implementations are not compatible

## Indented code blocks

    a simple
      indented code block
    ** this cannot be bold**

> as said above

## Fenced code blocks

```
<
 >
```

~~~
<
 >
~~~

   ```
   not indented
    indented
  aaa
   ```

```ruby
def foo(x)
  return 3
end
```

> Three text code blocks, and a code block linted in Ruby

```verilog
// Verilog
module top (/* ... */);
  /* ... */
```

```rust
// Rust
fn main() {
    println!("Hello, world!");
}
```

```assembly
# assembly
.text
main:
        la   $s0, A
        lw   $s0, 0($s0)
        la   $s1, B
        lw   $s1, 0($s1)
```
> Some tricky languages linting

## HTML blocks

<table><tr><td>
<pre>
**Hello**,

_world_.
</pre>
</td></tr></table>

> Hello, world

<pre language="haskell"><code>
import Text.HTML.TagSoup

main :: IO ()
main = print $ parseTags tags
</code></pre>

> Linted Haskell code

<style
  type="text/css">
h3 {color:red;}
</style>

> H3s are red; no display here

## Link reference definitions

[Foo*bar\]]:my_(url) 'title (with parens)'

[Foo*bar\]]

> foo -> title
>
> foo*bar] -> my_(url), with title

## Paragraphs

aaa
bbb

ccc
ddd

> two lines, not 4 or 5

# Container blocks

## Block quotes

   > # Foo
   > bar
  baz

> H1 foo, bar and baz in 1 line (laziness)

> - foo
- bar

> Foo in blockquote, bar in list item

>     code

>    not code

## List items

1.  foo

    ```
    bar
    ```

    baz

    > bam

> all in 1 list item

123456789. ok

1234567890. not ok

-1. not ok

> Less than 9 digits, non-negative

  1.  A paragraph
with two lines.

          indented code

      > A block quote.

# Inlines

## Code spans

`` foo ` bar ``

> foo ` bar in code

``
foo
bar  
baz
``

> No return

`<a href="`">`

<a href="`">`

`<http://foo.bar.`baz>`

<http://foo.bar.`baz>`

> Code, tag, code, link

## Emphasis and strong emphasis

**foo *bar **baz**
bim* bop**

> foo and bop are not italic

## Links

[link](foo(and(bar)))

[link](#Paragraphs)

> Two links

## Images

![foo *bar*]

[foo *bar*]: https://cyp0633-public-resource.oss-cn-qingdao.aliyuncs.com/_DSC5933.avif "Aiwan Pavilion"

![Aiwan Pavilion](https://cyp0633-public-resource.oss-cn-qingdao.aliyuncs.com/_DSC5933.avif)

## Autolinks

<https://cyp0633.icu>
