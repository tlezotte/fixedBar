JQUERY FIXED BAR
================

##Overview
Places a non-moving div bar on the top or bottom of the webpage.

##Instructions
```javascript
<script src="jquery-1.3.2.min.js" type="text/javascript"></script>
<!-- ===== Required files for jQuery Message Center ===== -->
<script src="jquery.fixedBar.js" type="text/javascript"></script>
<script type="text/javascript">
$(document).ready(function() {
$().fixedBar({
position: 'bottom',
height: '25',
style: 'customBar'
});
});
</script>
<!-- ===== End of Required files ===== -->
```

```html
<body>
<div id="fixeBar"></div>
</body>
```

##Arguments
`position: [‘bottom’, ‘top’]`  
*(Optional) String*  
A string that positions the fixedBar to the Top or Bottom of webpage.

`height: 25`  
*(Optional) Integer*  
A integer representing the height in pixels

`style: [‘ui-widget-content’, ‘custom‘]`  
*(Optional) String*  
A string representing a CSS class to customize fixedBar
