# MkDocs Configuration File

An example can be found at the [mkdocs-material demo](https://github.com/squidfunk/mkdocs-material/blob/master/mkdocs.yml)



Plugins:


MkDocs material theme is the most popular and rich on features

```yaml
theme:
  name: material
  features:
    - content.code.annotate
    - content.code.copy
    - content.tabs.link
    - header.autohide
    - announce.dismiss
    - navigation.footer
    - navigation.indexes
    - navigation.sections
    - navigation.tabs
    - navigation.top
    - navigation.tracking
    - search.share
    - search.suggest
    - search.highlight
    - content.action.edit
    
  # Dark and light mode, defaults to system theme
  palette:
    - media: "(prefers-color-scheme)"
      toggle:
        icon: material/link
        name: Switch to light mode
    - media: "(prefers-color-scheme: light)"
      scheme: default
      primary: indigo
      accent: indigo
      toggle:
        icon: material/toggle-switch
        name: Switch to dark mode
    - media: "(prefers-color-scheme: dark)"
      scheme: slate
      primary: black
      accent: indigo
      toggle:
        icon: material/toggle-switch-off
        name: Switch to system preference
```

Markdown extensions from material theme

```yaml
markdown_extensions:
  - pymdownx.highlight:
      anchor_linenums: true
      line_spans: __span
      pygments_lang_class: true
  - admonition
  - pymdownx.details
  - pymdownx.superfences:
      custom_fences:
        - name: mermaid
          class: mermaid
          format: !!python/name:pymdownx.superfences.fence_code_format
  - pymdownx.inlinehilite
  - pymdownx.snippets
```

Used plugins

```yaml
plugins:
  # Enables search
  - search
  # Enables export as PDF
  - pdf-export
  # Allows to add a whole directory in the navigation instead of just files
  # Sub-nav items are automatically created if the provided dir contains subdirectories 
  - include_dir_to_nav
  # Include content of other files in markdown
  - include-markdown:
      encoding: ascii
      preserve_includer_indent: false
      dedent: false
      trailing_newlines: true
      comments: true
      rewrite_relative_urls: true # true is default
      heading_offset: 0
      opening_tag: "{%"
      closing_tag: "%}"
      start: <!--start-->
      end: <!--end-->
```


Allow to edit pages

```yaml
repo_url: https://github.com/zebbra/neops-docs
edit_uri: edit/master
```


Social Media links in the footer

```yaml
extra:
  social:
    - icon: fontawesome/brands/mastodon
      link: https://neops.io
      name: Neops
```

Add a copyright by Zebbra

```yaml
copyright: Copyright &copy; Zebbra AG
```