# Minimal HTML Boilerplate
The following is my usual starting point for a fresh html file.
This should be compatible with all modern browsers from IE9 upwards, although I've not tested with all.

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    
    <!-- viewport meta tag improves rendering on mobile devices -->
    <!-- but we must now cope with narrow screens -->
    <meta name="viewport" content="width=device-width, initial-scale=1">
    
    <!-- other meta tags -->
    <meta name="author" content="name">
    <meta name="description" content="description here">
    <meta name="keywords" content="keywords,here">
    
    <!-- title shown on browser tab -->
    <title>tab title</title>
    
    <!-- favicon definition (16x16 pixel square icon) -->
    <link rel="shortcut icon" type="image/png" href="favicon.png">
    
    <!-- external stylesheet -->
    <link rel="stylesheet" type="text/css" href="stylesheet.css">
    
    <!-- inline stylesheet -->
    <style type="text/css">
    </style>
    
    <!-- external javascript -->
    <script type="application/javascript" src="javascript.js"></script>
  </head>
  
  <body>
    <!-- page content start -->
    <!-- page content ends -->
    
    <!-- run some javascript on page load complete -->
    <script type="application/javascript">
      function autorun() {
      }
      
      window.addEventListener("load", autorun, false);
    </script>

  </body>
</html>
```

Once copied I'll delete anything I don't want for a particular project.
