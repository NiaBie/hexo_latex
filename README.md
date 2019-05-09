## mathjax

```html
<!DOCTYPE html>
<script type="text/javascript" src="https://cdn.bootcss.com/mathjax/2.7.1/latest.js?config=TeX-AMS-MML_HTMLorMML"></script>

<script type="text/javascript">
  $(document).ready(function()
  {
    MathJax.Hub.Config(
    {
      tex2jax:
      {
        inlineMath: [
          ['$', '$'],
          ["\\[", "\\]"]
        ],
        processEscapes: true,
        skipTags: ['script', 'noscript', 'style', 'textarea', 'pre', 'code']
      }
    })

    MathJax.Hub.Queue(function()
    {
      var all = MathJax.Hub.getAllJax(),
      i;
      for (i = 0; i < all.length; i += 1)
      {
        all[i].SourceElement().parentNode.className += ' has-jax';
      }
    })
  });
</script>
```

### bug

## Katex

```html
<!DOCTYPE html>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/hexo-simple-theme/hexo_latex@1.0.0/katex/dist/katex.min.css" integrity="sha384-dbVIfZGuN1Yq7/1Ocstc1lUEm+AT+/rCkibIcC/OmWo5f0EA48Vf8CytHzGrSwbQ" crossorigin="anonymous">

<!-- The loading of KaTeX is deferred to speed up page rendering -->
<script defer src="https://cdn.jsdelivr.net/gh/hexo-simple-theme/hexo_latex@1.0.0/katex/dist/katex.min.js" integrity="sha384-2BKqo+exmr9su6dir+qCw08N2ZKRucY4PrGQPPWU1A7FtlCGjmEGFqXCv5nyM5Ij" crossorigin="anonymous"></script>

<!-- To automatically render math in text elements, include the auto-render extension: -->
<script defer src="https://cdn.jsdelivr.net/gh/hexo-simple-theme/hexo_latex@1.0.0/katex/dist/contrib/auto-render.min.js" integrity="sha384-kWPLUVMOks5AQFrykwIup5lo0m3iMkkHrD0uJ4H5cjeGihAutqP0yW0J6dpFiVkI" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>

<script>
$(document).ready(function () { // jqueryj
  renderMathInElement(document.body, {
    // ...options...
    delimiters: [
      { left: "$$", right: "$$", display: true },
      { left: "$", right: "$", display: false },
      { left: "\\[", right: "\\]", display: true }
    ]
  });
});
</script>
```

### bug

md中不能有换行,会被替换成`<br>`,katex无法渲染
