## 要求 

- 实现一个基础的计时器应用，点击开始按钮开始计时，点击结束按钮结束计时，并把计时的结果显示在上面的输入框中。

```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>定时器示例</title>
  </head>
  <body>
  
  <input type="text" id="result">
  
  <input type="button" value="开始" >
  <input type="button" value="结束" >
  
  <script>
	var date1,date2,intveral;
    function startTime(){
        date1 = new Date().getTime();
    }
	function displayTime(){
		var date = new Date().getTime();
		document.getElementById("result").innerHTML=date-date1+"毫秒";
	}
	function endTime(){
		date2 = new Date().getTime();
		document.getElementById("result").innerHTML=date2-date1+"毫秒";
	}
    function start(){
        startTime();
		intveral = setInterval("displayTime()",100);
    }
    function end(){
		clearInterval(intveral);
        endTime();
    }
</script>
  </body>
  </html>
```
