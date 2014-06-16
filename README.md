Cache Buster
====================

This dotCMS 2.5+ velocity macro is intended to allow for the addition of script and link tags to your HMTL with a timestamp at the end of the src/href to force browsers to re-download your file when you have updated it. 

To use this macro follow these easy steps:

1. Include the cache-buster.vtl file
2. Call the macro where you want the file to be includes

Here is an example of what the include code will look like
```
## cacheBuster( "File/Path" 'js or css' 'media-if css' )

#cacheBuster( '/css/sweet-sweet-styles.css' 'css' 'print' )
## outputs <link type="text/css" rel="stylesheet" href="/css/sweet-sweet-styles.css?00000000000000" media="print" />

#cacheBuster( '/js/awesome-script.js' 'js' )
## outputs <script type="text/javascript" src="/js/awesome-script.js?00000000000000"></script>
```

Note the "00000000000000" will be a time stamp of the last time that the file was edited. 

And that is it. Happy coding!
