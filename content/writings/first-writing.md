---
title: "First Writing"
date: 2026-02-24
draft: false
summary: "How this site stitches thoughts, visuals, and conversation together."
---

Writing in public begins with experimenting on the page itself. This site is a little operating system for ideas: each layout block is hand-tuned, the Markdown is honest, and the UI leans on a minimalist palette so the machinery fades into the background. That setup makes it easy to drop in a new paragraph, embed, or command and immediately see the effect.

<div class="feature-card">
  <p class="feature-title">Video</p>
  <p class="feature-lead">A paragraph about how this page handles video: text frames the purpose, then the embed follows so the viewer sees the clip in context.</p>
  <p>Below is an embedded Rick Astley clip (yes, the classic). The iframe is centered, sized for the column, and padded so the controls never overlap the surrounding copy.</p>
  <div class="feature-video">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/dQw4w9WgXcQ" title="Rick Astley - Never Gonna Give You Up" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</div>

<div class="feature-card">
  <p class="feature-title">Code</p>
  <p class="feature-lead">This is where the syntax highlighting kicks in—Goldmark passes the fenced block to Hugo’s highlighter, and the theme applies friendly colors.</p>
  <p>The snippet below follows the same structure as the hero section and proves that you can drop any language (C++ in this case) into a card and let the highlighter automatically color the keywords.</p>
  {{< highlight cpp >}}
#include <iostream>

int main() {
  std::cout << "Hello, world from 0xPaper!" << std::endl;
  return 0;
}
  {{< /highlight >}}
</div>
