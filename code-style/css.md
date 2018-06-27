# Skore CSS

## Contents

1. [General](#general)
2. [Formatting](#formatting)
3. [Comments](#comments)
4. [JavaScript hooks](#javascript-hooks)
5. [Performance](#performance)
  - 5.1. [Specificity](#specificity)
6. [References](#references)


<a name='general'></a>
## 1. General

- **a.** Use soft-tabs with a 2 spaces for indentation.
- **b.** Trim trailing white space on save.
- **c.** Set encoding file to UTF-8.
- **d.** Add new line at end of files.
- **e.** Declarations sorted alphabetically.
- **f.** Use lowercase and dashes in classes names, not underscores or camelCase.
- **g.** Do not use ID selectors.
- **h.** Use a semicolon after every declaration, including the last item.
- **i.** When using multiple selectors in a rule declaration, give each selector its own line.
- **j.** Put a space before the opening brace `{` in rule declarations.
- **k.** In properties, put a space after, but not before, the `:` character.
- **l.** Put closing braces `}` of rule declarations on a new line.
- **m.** Separate rules by new lines.
- **n.** Use single quotation marks for attribute selectors and property values.


**Bad**

```css
#my_selector{
    height:120px;
    display : block;
    padding: 10px 15px
}
div, p
{
    font-family: "open sans", sans-serif;
    text-align: center }
```

**Good**

```css
.my-selector {
  display: block;
  height: 120px;
  padding: 10px 15px;
}

div,
p {
  font-family: 'open sans', sans-serif;
  text-align: center;
}
```

---

<a name='formatting'></a>
## 2. Formatting

- **a.** Prefer hex color codes.
- **b.** Use shorthand hex values where available.
- **c.** Uppercase all hex values.
- **d.** All colors must be set on configuration files and must be used like variables.
- **e.** Avoid using shorthand properties for only one value.
- **f.** Use a leading zero in decimal numbers.
- **g.** Use `0` to specify that a style has no border.
- **h.** Avoid specifying units for 0 values.
- **i.** Use shorthand when appropriate.
- **j.** Avoid unnecessary shorthand declarations.


**Bad**

```css
.selector {
  background: #ff9933;
  border: none;
  color: rgb(90,90,90);
  margin-bottom: 10px;
  margin-left: 20px;
  margin-right: 10px;
  opacity: .5;
  padding: 0px 0px 15px;
}
```

**Good**

```css
.selector {
  background-color: #F93;
  border: 0;
  color: #5A5A5A;
  margin: 0 20px 10px 10px;
  opacity: 0.5;
  padding-bottom: 15px;
}
```

---

<a name='comments'></a>
## 3. Comments

Don't write comments. Ever.

---

<a name='javascript-hooks'></a>
## 4. JavaScript hooks

Prefixed with `.js-`:

```html
<button class='my-selector js-request-lessons-list'>Lessons List</button>
```

---

<a name='performance'></a>
## 5. Performance

<a name='specificity'></a>
### 5.1 Specificity

Although in the name (cascading style sheets) cascading can introduce unnecessary performance overhead for applying styles. For example:

```css
ul.user-list li span a:hover {
  color: red;
}
```

Styles are resolved during the renderer's layout pass. The selectors are resolved right to left, exiting when it has been detected the selector does not match.

If we want to give all `a` elements inside the `.user-list` red on hover, we can simplify this style to:

```css
.user-list > a:hover {
  color: red;
}
```

And if we want to only style specific `a` elements inside `.user-list`, we can give them a specific class:

```css
.user-list > .user-link:hover {
  color: red;
}
```

---

<a name='references'></a>
## 6. References

* [Airbnb](https://github.com/airbnb/css)
* [Google](https://google.github.io/styleguide/htmlcssguide.xml#CSS_Formatting_Rules)
* [Trello](https://gist.github.com/bobbygrace/9e961e8982f42eb91b80)
* [thoughtbot](https://github.com/thoughtbot/guides/tree/master/style/sass)
* [Primer](http://primercss.io/guidelines/#scss)
* [Code Guide](http://codeguide.co/)
