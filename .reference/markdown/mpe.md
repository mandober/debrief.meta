# Table of Contents

Markdown Preview Enhanced can create TOC for your markdown file.

cmd-shift-p then choose Markdown Preview Enhanced:
`Create Toc` to create TOC.
That will insert:

`<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->`

- Multiple TOCs can be created.
- To exclude a heading from the TOC, append `{ignore=true}` after your heading.
- The TOC will be updated when you save the markdown file. 
- You need to keep the preview open to get TOC updated.

## Configuration

- `orderedList` Use orderedList or not
- `depthFrom` [1-6] inclusive
- `depthTo` [1-6] inclusive
- `ignoreLink` If set to true, then TOC entry will not be hyperlinks

You can also create TOC by inserting `[TOC]` to your markdown file.

```
[TOC]

# Heading 1

## Heading 2 {ignore=true}

Heading 2 will be ignored from TOC.
```

However, this way will only display TOC in preview, while leaving editor content unchanged.


## TOC and Sidebar TOC Configuration

You can configure `[TOC]` and sidebar TOC by writting front-matter:

```yaml
---
toc:
  depth_from: 1
  depth_to: 6
  ordered: false
---
```

