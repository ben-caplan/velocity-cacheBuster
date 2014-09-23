Cache Buster
====================

This dotCMS 2.5+ velocity macro is intended to allow for the addition of script and link tags to your HMTL with a timestamp at the end of the src/href to force browsers to re-download your file when you have updated it.

To use this macro follow these easy steps:

1. Include the cache-buster.vtl file
2. Call the macro where you want the file to be included

Here are examples of what the include code will look like:

```
## cacheBuster( "file path" 'js or css' 'media if CSS or asynchronous loading attribute if JS' )

#cacheBuster( '/css/sweet-sweet-styles.css' 'css' )
## outputs <link type="text/css" rel="stylesheet" href="/css/sweet-sweet-styles.css?00000000000000">

#cacheBuster( '/css/sweet-print-styles.css' 'css' 'print' )
## outputs <link type="text/css" rel="stylesheet" href="/css/sweet-print-styles.css?00000000000000" media="print">

#cacheBuster( '/js/awesome-script.js' 'js' )
## outputs <script type="text/javascript" src="/js/awesome-script.js?00000000000000"></script>

#cacheBuster( '/js/awesome-asynchronous-script.js' 'js' 'async')
## outputs <script async type="text/javascript" src="/js/awesome-asynchronous-script.js?00000000000000"></script>
```

_Note the "00000000000000" will be a time stamp of the last time that the file was edited._

And that is it. Happy coding!
