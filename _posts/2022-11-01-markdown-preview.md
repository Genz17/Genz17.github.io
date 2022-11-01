---
title:  "Markdown Preview in NeoVim"
layout: archive
---

When I switch to Neovim, I find it hard for me to install the markdown-preview
plugins.

So I just start to use `grip`.

Just run 

```
pip install grip
```

And then use grip to create the preview window in your browser:
```
grip *.md [port]
```

Enjoy! The only bad thing is that `grip` can not provide a real-time preview.
You need to save the markdown file after any adjustment to see the output.
