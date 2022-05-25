# js-script-to-clear-cache
js script to clear cache

```js
  var scripts =  document.getElementsByTagName('script');
var torefreshs = ['script.js', 'core.min.js'] ; // list of js to be refresh
var key = (new Date()).getTime(); // change this key every time you want force a refresh

for(var i=0;i<scripts.length;i++){ 
   for(var j=0;j<torefreshs.length;j++){ 
      if(scripts[i].src && (scripts[i].src.indexOf(torefreshs[j]) > -1)){
        new_src = scripts[i].src.replace(torefreshs[j],torefreshs[j] + '?k=' + key );
        scripts[i].src = new_src; // change src in order to refresh js
      } 
   }
}




var scripts =  document.getElementsByTagName('link');
var torefreshs = ['bootstrap.css', 'style.css','novi.css','style-meeypage.css'] ; // list of js to be refresh
var key = (new Date()).getTime(); // change this key every time you want force a refresh
for(var i=0;i<scripts.length;i++){ 
   for(var j=0;j<torefreshs.length;j++){ 
      if(scripts[i].href && (scripts[i].href.indexOf(torefreshs[j]) > -1)){
        new_href = scripts[i].href.replace(torefreshs[j],torefreshs[j] + '?k=' + key );
        scripts[i].href = new_href; // change href in order to refresh js
      } 
   }
}


```
