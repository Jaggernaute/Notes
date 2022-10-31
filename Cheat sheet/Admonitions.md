## Keywords:

| type     | aliases                           |
| -------- | --------------------------------- |
| note     | `note`, `seealso`                 |
| abstract | `abstract`, `summary`, `tldr`     |
| info     | `info`, `todo`                    |
| tip      | `tip`, `hint`, `importan`         |
| success  | `success`, `check`, `done`        |
| question | `question`, `help`, `faq`         |
| warning  | `warning`, `caution`, `attention` |
| failure  | `failure`, `fail`, `missing`      |
| danger   | `danger`, `error`                 |
| bug      | `bug`                             |
| example  | `example`                         |
| quote    | `quote`,`cite`                    |

## Examples
**Notes:**
```ad-note 
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.
```
**Abstract:**
```ad-abstract
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.
```
**Info:**
```ad-info
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.
```
**Tip:**
```ad-tip
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.
```
**Success:**
```ad-success
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.
```
**Question:**
```ad-question
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.
```
**Warning:**
```ad-warning
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.
```
**Failure:**
```ad-failure
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.
```
**Danger:**
```ad-danger
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.
```
**Bug:**
```ad-bug
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.
```
**Example:**
```ad-example
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.
```
**Quote:**
```ad-quote
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.
```

## Formatting:

```ad-<type> # Admonition type. See below for a list of available types.
title:                  # Admonition title.
collapse:               # Create a collapsible admonition.
icon:                   # Override the icon.
color:                  # Override the color.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla.

```

**Title :**
```ad-note
title: Title
Change the title of the notes
```
```ad-note
title: $\sum^{\infty}_{n=0}n+1$
The titles support the full obsidian markdown syntax
```
```ad-note
title:
To create a note without a title feild just leave it blank
```
```ad-note
title: You can even just put a title
```
**Collapse :**
```ad-note
title: Opened note
collapse: open
Default position = open
```
```ad-note
title: Closed note
collapse: close
Default position = close
```
**Colors:**
```ad-note
color: 200, 200, 200
Colors can be changed by inputing the RGB value
```
**No content:**
```ad-note
```
**Nesting:**
`````ad-note
title: Nested Admonitions
collapse: open

Hello!
````ad-note
title: This admonition is nested.
This is a nested admonition!

```ad-warning
title: This admonition is closed.
collapse: close
But it has content.
```

````

This is in the original admonition.
`````
**Code blocks:**
```ad-bug
title: Here is a lil' bug:
This is a bug :
~~~java
System.out.println("Error lol !");
~~~
It can lead to :
```ad-danger
title: remote code execution:
[Folina](https://securelist.com/cve-2022-30190-follina-vulnerability-in-msdt-description-and-counteraction/106703/)
```
````