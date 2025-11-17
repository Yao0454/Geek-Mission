# JS学习记录

## 变量声明
```javascript
let name = "枫枫子";   // 可以改
const age = 20;       // 不能改
var old = "别用";     // 容易出bug

// 和python不一样，js要声明类型
```

## 数据类型
```javascript
let num = 42;          // 数字，没有int float区分
let str = "Hello";     // 字符串
let bool = true;       // 布尔
let arr = [1,2,3];     // 数组，像python的list
let obj = {name: "JS"}; // 对象，像python的dict

// js特有的：
let nothing = null;      // 空
let undef = undefined;   // 未定义，容易搞混
```

## 函数
```javascript
// 普通写法
function hello(name) {
    return "hi " + name;
}

// 箭头函数，简洁点
const hello2 = (name) => "hi " + name;

// 调用
hello("小明");  // "hi 小明"
```

## if判断
```javascript
let score = 85;
if (score >= 90) {
    console.log("优秀");
} else if (score >= 80) {
    console.log("还行");
} else {
    console.log("菜");
}

// 简写
let result = score >= 60 ? "过了" : "挂了";
```

## 循环
```javascript
// 普通for
for (let i = 0; i < 5; i++) {
    console.log(i);
}

// 遍历数组
let arr = ["a", "b", "c"];
for (let item of arr) {
    console.log(item);  // a, b, c
}

// 遍历对象
let obj = {name: "小明", age: 18};
for (let key in obj) {
    console.log(key, obj[key]);  // name 小明, age 18
}
```

## 数组
```javascript
let arr = [1, 2, 3];

arr.push(4);       // 加到末尾 [1,2,3,4]
arr.pop();         // 删最后一个 [1,2,3]
arr.length;        // 长度 3

// 常用的
arr.map(x => x*2);      // 每个都乘2 [2,4,6]
arr.filter(x => x>1);   // 筛选 [2,3]
arr.includes(2);        // 有没有2 true

// 合并数组
let a = [1,2];
let b = [3,4];
let c = [...a, ...b];   // [1,2,3,4] 三个点是展开
```

## 对象
```javascript
let person = {
    name: "小明",
    age: 18,
    say: function() {
        console.log("hello");
    }
};

// 取值
person.name;        // "小明"
person["age"];      // 18

// 改值
person.age = 19;
person.city = "北京";  // 新增属性

// 删除
delete person.city;

// 解构，把对象拆开
let {name, age} = person;
console.log(name);  // "小明"
```

## 字符串
```javascript
let str = "hello world";

str.length;              // 长度 11
str.toUpperCase();       // "HELLO WORLD"
str.slice(0, 5);         // "hello" 截取
str.split(" ");          // ["hello", "world"] 分割

// 模板字符串，用反引号
let name = "小明";
let msg = `你好 ${name}`;  // "你好 小明"

// 多行
let text = `第一行
第二行
第三行`;
```

## DOM操作
```javascript
// 找元素
let btn = document.getElementById("btn1");
let div = document.querySelector(".box");

// 改内容
btn.textContent = "点我";
div.innerHTML = "<h1>标题</h1>";

// 改样式
btn.style.color = "red";
btn.style.backgroundColor = "blue";

// 点击事件
btn.addEventListener("click", function() {
    alert("被点了!");
});

// 简写
btn.onclick = () => alert("点了!");
```

## 容易搞错的地方
```javascript
// 类型转换很坑
"5" + 3;     // "53" 字符串拼接
"5" - 3;     // 2 数字减法
true + 1;    // 2

// 比较用三个=
"" == 0;     // true 坑爹
"" === 0;    // false 严格比较

// 转换类型
Number("123");   // 123
String(123);     // "123"
```

## 作用域
```javascript
// let有块作用域
if (true) {
    let x = 1;
}
console.log(x);  // 报错，x不存在

// var有函数作用域，容易出bug
function test() {
    if (true) {
        var y = 2;
    }
    console.log(y);  // 2，能访问到
}
```

## 一些新特性
```javascript
// 解构，把数组或对象拆开
let [a, b] = [1, 2];         // a=1, b=2
let {name, age} = person;     // 从对象取值

// 默认参数
function hello(name = "朋友") {
    return "你好 " + name;
}

// 展开运算符
let arr = [1, 2, 3];
let newArr = [...arr, 4, 5];  // [1,2,3,4,5]
```

## 写个简单例子
```javascript
// 计算器
function calc(a, b, op) {
    if (op === "+") return a + b;
    if (op === "-") return a - b;
    if (op === "*") return a * b;
    if (op === "/") return a / b;
    return "不知道这个操作";
}

calc(5, 3, "+");  // 8

// 处理学生成绩
let students = [
    {name: "小明", score: 85},
    {name: "小红", score: 92}
];

// 找高分的
let good = students.filter(s => s.score > 80);
console.log(good);

// 算平均分
let avg = students.map(s => s.score).reduce((a,b) => a+b) / students.length;
console.log("平均:", avg);
```

