# Responsive CSS Class

In this class we explored:
- The `@media` so-called **at-rule** in modern CSS
- The different, so-called **media types** (e.g. _screen_, _page_, etc.)
- The different, so-called **media features** (e.g. _min-width_, _max-width_, _prefers-color-scheme_, _pointer_, etc.)

The syntax for a media query:
```Mustache
[[{{not|only}}] {{mediatype}}] [{{and|or}}] [({{mediafeature}}: {{mediafeaturevalue}}) ]...
```

From the syntax above, we can say that a media query:
- Can optionally start with either `only` or `not`, followed by a **media type** (e.g. _screen_, _page_, etc.)
- If we start with the above, then we need the keyword `and` to combine the media type with one or more **media feature rules**
- A media feature rule is enclosed in parantheses `(...)` and in between we have one of the possible **media features** followed by a colon and the desired **media feature value**.
- In case of more than one **media feature rules** they have to be combined with either `and` or `or` to decide the logical relationship between these rules (e.g. do you want them all to apply, or only some of them)

Media queries can be nested, such as most other at-rules in CSS. Example:
```CSS
@media only screen {
    @media (prefers-color-scheme: dark) {
        /* CSS declarations here apply only to dark mode on the screen */
    }
}
```
