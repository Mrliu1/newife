这部分涉及的是数组的遍历以及拼字符串，以及上一blog的innerHTML和outerHTML.
1、数组遍历传统的for。
2、es5 新增的forEach（）、map()方法，里面都是传一个回调函数，回调函数的值为function(currentValue,index,targetArr);
3、forEach()的特点。
forEach方法返回值undefined。实现 forEach()除了抛出异常外，没有办法停止或打破循环。即：你不能使用break语句中断循环，也不能使用return语句返回到外层函数。如果您需要这样的行为，该forEach()方法是错误的工具。用一个简单的循环或for ...来  代替。如果您正在为谓词测试数组元素并需要布尔返回值，则可以使用every()or some()替代。如果可用的话，新的方法find()或者findIndex()可以用于提前终止真正的谓词
    // forEach和map一样是传回调函数[2, 5, , 9].forEach(logArrayElements)，回调函数的参数为（element, index, array），当前元素，index下标，目标数组。
4、map() 的特点。
  //使用map的方法实现，返回一个新数组,map返回后是可以在进行遍历的
  /*  eg:var kvArray = [{key: 1, value: 10}, 
               {key: 2, value: 20}, 
               {key: 3, value: 30}];

var reformattedArray = kvArray.map(obj =>{ 
   var rObj = {};
   rObj[obj.key] = obj.value;
   return rObj;
})*/
5、es6对于对象下标遍历可使用for。。。in ,他也可以遍历数组的下标；
6、es6属于数组的遍历可使用for。。。of，他可以遍历Set,和Map的集合数组
7、es6提供了一个将对象的key转化为数组的方法，Object.keys;
8、es66提供了一个将对象的value转化为数组的方法，Object.values;
9、es6解构
10、...扩展运算符，可以解析数组，字符串，类似数组对象，如果没有部署 Iterator 接口，就使用Array.from方法将arrayLike转为真正的数组。 Map 和 Set 结构， Generator 函数是可以直接使用。。。的。
let aa='qwrtwtwert';[...aa]
(10) ["q", "w", "r", "t", "w", "t", "w", "e", "r", "t"]//字符串转化为数组；==Array.from(aa)
11，Array.from一般与new Set(),创建一个去重的数组
eg:
cc= ["q", "w", "r", "t", "w", "t", "w", "e", "r", "t"];
let dd=Array.from(new Set(cc));console.log(1,dd);
打印出：1 (5) ["q", "w", "r", "t", "e"]