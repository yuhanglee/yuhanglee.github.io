# Markdown Syntax Guide


This article offers a sample of basic Markdown syntax that can be used in Hugo content files, also it shows whether basic HTML elements are decorated with CSS in a Hugo theme.

&lt;!--more--&gt;

## Headings

The following HTML `&lt;h1&gt;`—`&lt;h6&gt;` elements represent six levels of section headings. `&lt;h1&gt;` is the highest section level while `&lt;h6&gt;` is the lowest.

# H1
## H2
### H3
#### H4
##### H5
###### H6

## Paragraph

Xerum, quo qui aut unt expliquam qui dolut labo. Aque venitatiusda cum, voluptionse latur sitiae dolessi aut parist aut dollo enim qui voluptate ma dolestendit peritin re plis aut quas inctum laceat est volestemque commosa as cus endigna tectur, offic to cor sequas etum rerum idem sintibus eiur? Quianimin porecus evelectur, cum que nis nust voloribus ratem aut omnimi, sitatur? Quiatem. Nam, omnis sum am facea corem alique molestrunt et eos evelece arcillit ut aut eos eos nus, sin conecerem erum fuga. Ri oditatquam, ad quibus unda veliamenimin cusam et facea ipsamus es exerum sitate dolores editium rerore eost, temped molorro ratiae volorro te reribus dolorer sperchicium faceata tiustia prat.

Itatur? Quiatae cullecum rem ent aut odis in re eossequodi nonsequ idebis ne sapicia is sinveli squiatum, core et que aut hariosam ex eat.

## Blockquotes

The blockquote element represents content that is quoted from another source, optionally with a citation which must be within a `footer` or `cite` element, and optionally with in-line changes such as annotations and abbreviations.

### Blockquote without attribution

&gt; Tiam, ad mint andaepu dandae nostion secatur sequo quae.
&gt; **Note** that you can use *Markdown syntax* within a blockquote.

### Blockquote with attribution

&gt; Don&#39;t communicate by sharing memory, share memory by communicating.&lt;br&gt;
&gt; — &lt;cite&gt;Rob Pike[^1]&lt;/cite&gt;

[^1]: The above quote is excerpted from Rob Pike&#39;s [talk](https://www.youtube.com/watch?v=PAAkCSZUG1c) during Gopherfest, November 18, 2015.

## Tables

Tables aren&#39;t part of the core Markdown spec, but Hugo supports supports them out-of-the-box.

   Name | Age
--------|------
    Bob | 27
  Alice | 23

### Inline Markdown within tables

| Italics   | Bold     | Code   |
| --------  | -------- | ------ |
| *italics* | **bold** | `code` |

| A                                                        | B                                                                                                             | C                                                                                                                                    | D                                                 | E                                                          | F                                                                    |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|------------------------------------------------------------|----------------------------------------------------------------------|
| Lorem ipsum dolor sit amet, consectetur adipiscing elit. | Phasellus ultricies, sapien non euismod aliquam, dui ligula tincidunt odio, at accumsan nulla sapien eget ex. | Proin eleifend dictum ipsum, non euismod ipsum pulvinar et. Vivamus sollicitudin, quam in pulvinar aliquam, metus elit pretium purus | Proin sit amet velit nec enim imperdiet vehicula. | Ut bibendum vestibulum quam, eu egestas turpis gravida nec | Sed scelerisque nec turpis vel viverra. Vivamus vitae pretium sapien |

## Code Blocks
### Code block with backticks

```html
&lt;!doctype html&gt;
&lt;html lang=&#34;en&#34;&gt;
&lt;head&gt;
  &lt;meta charset=&#34;utf-8&#34;&gt;
  &lt;title&gt;Example HTML5 Document&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;p&gt;Test&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
```

### Code block indented with four spaces

    &lt;!doctype html&gt;
    &lt;html lang=&#34;en&#34;&gt;
    &lt;head&gt;
      &lt;meta charset=&#34;utf-8&#34;&gt;
      &lt;title&gt;Example HTML5 Document&lt;/title&gt;
    &lt;/head&gt;
    &lt;body&gt;
      &lt;p&gt;Test&lt;/p&gt;
    &lt;/body&gt;
    &lt;/html&gt;

### Diff code block

```diff
[dependencies.bevy]
git = &#34;https://github.com/bevyengine/bevy&#34;
rev = &#34;11f52b8c72fc3a568e8bb4a4cd1f3eb025ac2e13&#34;
- features = [&#34;dynamic&#34;]
&#43; features = [&#34;jpeg&#34;, &#34;dynamic&#34;]
```

### One line code block

```html
&lt;p&gt;A paragraph&lt;/p&gt;
```

## List Types

### Ordered List

1. First item
2. Second item
3. Third item

### Unordered List

* List item
* Another item
* And another item

### Nested list

* Fruit
  * Apple
  * Orange
  * Banana
* Dairy
  * Milk
  * Cheese

## Other Elements — abbr, sub, sup, kbd, mark

&lt;abbr title=&#34;Graphics Interchange Format&#34;&gt;GIF&lt;/abbr&gt; is a bitmap image format.

H&lt;sub&gt;2&lt;/sub&gt;O

X&lt;sup&gt;n&lt;/sup&gt; &#43; Y&lt;sup&gt;n&lt;/sup&gt; = Z&lt;sup&gt;n&lt;/sup&gt;

Press &lt;kbd&gt;CTRL&lt;/kbd&gt; &#43; &lt;kbd&gt;ALT&lt;/kbd&gt; &#43; &lt;kbd&gt;Delete&lt;/kbd&gt; to end the session.

Most &lt;mark&gt;salamanders&lt;/mark&gt; are nocturnal, and hunt for insects, worms, and other small creatures.

---

> 作者: [liyuhang](https://github.com/yuhanglee)  
> URL: https://yuhanglee.github.io/posts/markdown-syntax/  

