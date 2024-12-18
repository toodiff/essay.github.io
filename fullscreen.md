# Detect fullscreen mode used in javascript

```javascript
//初始化
var browserIsFullScreen = window.matchMedia('(display-mode: fullscreen)').matches;

//监听
window.matchMedia('(display-mode: fullscreen)').addEventListener('change', function(options){
  if (options.matches) {
    browserIsFullScreen = true;
  } else {
    browserIsFullScreen = false;
  }
});
```
