## 要求 

- 补充以下HTML，实现点击某一个数字可以alert出该数字。

```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>事件监听</title>
  </head>
  <body>
  
  <ul id="no">
      <li>1</li>
      <li>2</li>
      <li>3</li>
      <li>4</li>
      <li>5</li>
      <li>6</li>
      <li>7</li>
  </ul>
  
  <script>
     var item = document.getElementsByTagName("li");
	 for (var i=0;i<item.length;i++){
		item[i].index=i;
		item[i].onclick=function(){
			alert(this.index+1);
		}
	 }
  </script>
  </body>
  </html>
```
