本人的一个百度的课程题目，实现的是输入数据显示在其他地方。这里涉及的知识有。
1、事件监听。addEventListener('click',function(){})
2、js获取都dom元素，document.getElementById('aa')//获取id为aa的dom
		    document.getElementsByClassName('bb');//获取.class为bb的dom
		    document.getElementsByTagName('p');//获取p标签；
3.使用querySelector,querySelector选择器js原生的有类似于和jQuery的$一样强大的选择绑定选择器的功能。
		document.querySelector("p")//取第一个P标签dom,
		document.querySelector(".app")//取第一个class为app的dom
		document.querySelector("#apps")//取id为apps的dom
4.// var _input =document.getElementById('aqi-input');
  var _input=document.querySelector('#aqi-input');
_input.getAttribute('value')//得到的值都是aa他是dom属性值，属性值不可变；_input.value取到的是HTML值，是可变的。
5.innerHTML和innerText的区别
innerHTML是符合W3C标准的属性，而innerText只适用于IE浏览器（现在也适应chrome浏览器）
6、可以使用innerHTML取得包含HTML标签的内容后，再用正则表达式去除HTML标签
正则去标签方法  var content = document.getElementById("p1");  
            alert(content.innerHTML.replace(/& lt;.+?>/gim,'')); 
7.label 和input的妙用， input的id和label的for设置为同样的值可以使点击label里的内容触发input的事件。