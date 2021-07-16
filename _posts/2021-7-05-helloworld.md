---
layout: post
title: HelloWorld
tags: 
- jekyll theme
- jekyll
math: true

---
HelloWorld

<img src="/h.png">

<script type="text/javascript">
    function Enter(e) {
        if (e.keyCode == 13) {
            var input1 = document.getElementById("input1");
            if (input1.value <= 0)
            {
                alert("请输入整数");
                return 
            }
        
            var result = document.getElementById("result");
            result.innerHTML=input1.value;

            input1.value="";
        }
    };

    function OK() {
        var input1 = document.getElementById("input1").value;
        if (input1 <= 0)
        {
           alert("请输入西瓜数量");
           return 
        }

        var input2 = document.getElementById("input2").value;
        if (input2 <= 0)
        {
            alert("请输入西红柿数量");
            return 
        }
    
        var number = Math.random();
        number = Math.ceil(number * 100); 
        var str = "没看到西红柿"
        var cnt = input1
        if (number < 50){
            str = "看到西红柿了"
            cnt = input2
        }
        
        str += ", 买了" + cnt + "个西瓜";

        var result = document.getElementById("result");
        result.innerHTML=str;
    };

</script>
买
<input id="input1" style="width: 30px" 
        onkeyup="this.value=this.value.replace(/\D/g,'')"  onafterpaste="this.value=this.value.replace(/\D/g,'')" 
        maxlength="1" placeholder=""> 
个西瓜，
如果看到西红柿，买
<input id="input2" style="width: 30px" onkeypress="Enter(event)"
        onkeyup="this.value=this.value.replace(/\D/g,'')"  onafterpaste="this.value=this.value.replace(/\D/g,'')" 
        maxlength="1" placeholder=""> 
个

<input id="Button1" type="button" value="确定" onclick="OK()" /> 

<p id="result"></p>
