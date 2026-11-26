---
title: "CSS, Blogger and Simple template transparency"
date: 2013-02-25
tags: ["Programming"]
description: "It may seem quite obvious for any HTML/CSS developer how to do this,  but I struggled for 2 hours to find out how to set a semi-transparent  background while using the Simple template of Blogger. Usually websites indicate how to do it while using the Dynamic template. My main problem was to know how the pane component was called internally. Finally I could find the solution in this thread from Bloggeries(http://www.bloggeries.com/)."
permalink: "/en/css-blogger-and-simple-template-transparency/"
---

It may seem quite obvious for any HTML/CSS developer how to do this,
but I struggled for 2 hours to find out how to set a semi-transparent
background while using the Simple template of Blogger. Usually websites
indicate how to do it while using the Dynamic template. My main problem
was to know how the pane component was called internally. Finally I could
find the solution in this [thread](http://www.bloggeries.com/forum/showthread.php?t=26163)
from Bloggeries(http://www.bloggeries.com/).

You must go to your Blogger configuration and click on **Template**.
Then click on **Customize. \*\*This will bring the template customization page.
Click then in \*\*Advance**, go to the bottom of the new categories pane and
click on **Add CSS**. Here you can add the following lines:

```
background-color: rgba(255, 255, 255, 0.7);
```

Change the **255** values to the RGB values you want for the background and
the **0.7** to the alpha setting you prefer (from **0.0** to **1.0**). Click
on **Apply to Blog** at the upper right corner and enjoy the benefits of alpha
blending in your blog!

Remember this is valid for the **Simple Template** of Blogger. I didn’t try
with other templates.

Please enable JavaScript to view the [comments powered by Disqus.](http://disqus.com/?ref_noscript)
[comments powered by Disqus](http://disqus.com)
