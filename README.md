# jquery.duoshuo.js
a jQuery plugin to load duoshuo comments likes and other data

## Dependence

* [jquery.js](https://jquery.com/)
* [pagecache.js](https://github.com/jokinkuang/pagecache.js)

## Usage

### use data-attr
\<span class="post-data" data-method="comments" data-short-name='jokin' data-thread-key="index" data-text=" · 评论 %s"> · 评论 0\</span>  
\<span class="post-data" data-method="reposts" data-short-name='jokin' data-thread-key="index" data-text=" · 转发 %s"> · 转发 0\</span>  

\<script src="http://cdn.bootcss.com/jquery/3.1.0/jquery.min.js">\</script>  
\<script src="pagecache.js">\</script>  
\<script src="jquery.duoshuo.js">\</script>  
```javascript
<script>
  $(".post-data").duoshuo();
</script>
```

### use settings
\<span class="post-comments"> · 评论 0\</span>  
\<span class="post-reposts"> · 转发 0\</span>  

\<script src="http://cdn.bootcss.com/jquery/3.1.0/jquery.min.js">\</script>  
\<script src="pagecache.js">\</script>  
\<script src="jquery.duoshuo.js">\</script>  
```javascript
<script>
  $.Duoshuo.settings = { shortName: "jokin", threadKey: "index"};
  $(".post-comments").duoshuo("comments", " · 评论 %s");
  $(".post-reposts").duoshuo("reposts", " · 转发 %s");
</script>
```

### use parameter
\<span class="post-comments"> · 评论 0\</span>  
\<span class="post-reposts"> · 转发 0\</span>  

\<script src="http://cdn.bootcss.com/jquery/3.1.0/jquery.min.js">\</script>  
\<script src="pagecache.js">\</script>  
\<script src="jquery.duoshuo.js">\</script>  
```javascript
<script>
  $(".post-comments").duoshuo("comments", " · 评论 %s", "index", "jokin");
  $(".post-reposts").duoshuo("reposts", " · 转发 %s", "index", "jokin");
</script>
```

## License

Under The [MIT](https://tldrlegal.com/license/mit-license) License
