---
icon: lucide/rocket
---

# Zensical w 5 minut

## Code Blocks

> Go to [documentation](https://zensical.org/docs/authoring/code-blocks/)

``` python hl_lines="2" title="Code blocks"
def greet(name):
    print(f"Hello, {name}!") # (1)!

greet("Python")
```

1.  > Go to [documentation](https://zensical.org/docs/authoring/code-blocks/#code-annotations)

    Code annotations allow to attach notes to lines of code.

Code can also be highlighted inline: `#!python print("Hello, Python!")`.

## Diagrams

> Go to [documentation](https://zensical.org/docs/authoring/diagrams/)

``` mermaid
graph LR
  A[Start] --> B{Error?};
  B -->|Yes| C[Hmm...];
  C --> D[Debug];
  D --> B;
  B ---->|No| E[Yay!];
```

## Footnotes

> Go to [documentation](https://zensical.org/docs/authoring/footnotes/)

Here's a sentence with a footnote.[^1]

Hover it, to see a tooltip.

[^1]: This is the footnote.


## Formatting

> Go to [documentation](https://zensical.org/docs/authoring/formatting/)

- ==This was marked (highlight)==
- ^^This was inserted (underline)^^
- ~~This was deleted (strikethrough)~~
- H~2~O
- A^T^A
- ++ctrl+alt+del++

## Icons, Emojis

> Go to [documentation](https://zensical.org/docs/authoring/icons-emojis/)

* :sparkles: `:sparkles:`
* :rocket: `:rocket:`
* :tada: `:tada:`
* :memo: `:memo:`
* :eyes: `:eyes:`

## Task Lists

> Go to [documentation](https://zensical.org/docs/authoring/lists/#using-task-lists)

* [x] Install Zensical
* [x] Configure `zensical.toml`
* [x] Write amazing documentation
* [ ] Deploy anywhere

## Tooltips

> Go to [documentation](https://zensical.org/docs/authoring/tooltips/)

[Hover me][example]

  [example]: https://example.com "I'm a tooltip!"

<div class="grid cards" markdown>

-   :material-link-variant: &nbsp; **Link Intelligence**

    ---

    Jak wygenerować własną statyczną stronę internetową.

-   :material-eye-outline: &nbsp; **Markdown Preview**

    ---

    Jak za darmo ją opublikować i utrzymywać.

-   :material-format-text: &nbsp; **Markdown Formatter**

    ---

    Jak praktycznie wykorzystać automatyzację do weryfikacji i publikacji zmian na swojej stronie.

-   :material-alert-outline: &nbsp; **Markdown Linter** <small>coming soon</small>

    ---

    Workspace-wide diagnostics, including cross-file link tracking and analysis, and structural and prose linting for common Markdown issues.

</div>