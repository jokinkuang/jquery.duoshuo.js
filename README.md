# jquery.duoshuo.js
a jQuery plugin to load duoshuo comments、likes、reposts、views and so on

## Dependence

* [jquery.js](https://jquery.com/)
* [pagecache.js](https://github.com/jokinkuang/pagecache.js)

## Usage

### use data-attr
\<span class="post-data" data-method="comments" data-short-name='jokin' data-thread-key="index" data-text=" · 评论 %s"> · 评论 0\</span>  
\<span class="post-data" data-method="reposts" data-short-name='jokin' data-thread-key="index" data-text=" · 转发 %s"> · 转发 0\</span>  

\<script src="[http://cdn.bootcss.com/jquery/3.1.0/jquery.min.js]()">\</script>  
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

\<script src="[http://cdn.bootcss.com/jquery/3.1.0/jquery.min.js]()">\</script>  
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

\<script src="[http://cdn.bootcss.com/jquery/3.1.0/jquery.min.js]()">\</script>  
\<script src="pagecache.js">\</script>  
\<script src="jquery.duoshuo.js">\</script>  
```javascript
<script>
  $(".post-comments").duoshuo("comments", " · 评论 %s", "index", "jokin");
  $(".post-reposts").duoshuo("reposts", " · 转发 %s", "index", "jokin");
</script>
```

### priority
data-attr < settings < parameter
> parameter override the settings, settings override the data-attr


### default settings object
```javascript
  {
    attrText: "data-text",
    attrKey: "data-thread-key",
    attrName: "data-short-name",
    defaultSymbol: "%s",
    domain: "http://api.duoshuo.com",
    shortName: "",
  }
```
> you can override the settings by `$.Duoshuo.settings = {}`


### function call
> $(selector).duoshuo([[[["method"], "text"], "thread_key"], "short_name"])


## License

Under The [MIT](https://tldrlegal.com/license/mit-license) License
