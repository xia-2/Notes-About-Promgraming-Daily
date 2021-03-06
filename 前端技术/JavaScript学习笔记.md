# JavaScript学习笔记

时间投入合计：4小时07分钟

2.3 1个小时左右

2.4  1个小时33分钟

2.4  33分钟

2.12   34分钟

2.14  27 分钟

   

## 提示：

1. **把脚本置于元素的底部，可改善显示速度，因为脚本编译会拖慢显示。**

2. **旧的 JavaScript 例子也许会使用 type 属性：<script type="text/javascript">。**

   **注释：type 属性不是必需的。JavaScript 是 HTML 中的默认脚本语言。**
   
3. **外部脚本不能包含  标签。**

4. **script标签一般放置在head或者body里面。**

5. **JavaScript支持折行书写，只要在这条语句结束时加上“；”就行**。

6. **字符串之间可以直接用加法进行运算，等效于拼接在一起。多个空格会被认为是一个空格。**

   **"Bill" + " " + "Gates"，计算为 "Bill Gates"**

7. **双斜杠 // 或 /* 与 */*之间的代码被视为注释***

8. **JavaScript 对大小写敏感 ,所有 JavaScript 标识符\*对大小写敏感\*,**

   **变量 lastName 和 lastname，是两个不同的变量。**

------
1. innerHTML 返回某个开始和结束标签之间的 HTML

2. obj.属性(html元素的属性)来改变原来的属性值
   - obj.src='/i/eg_bulbon.gif'  修改图片的指向
   - obj.style.something 来修改样式
   
------

## Day1 开始时间：23:00

   #### JavaScript 能够以不同方式“显示”数据：

   - 使用 window.alert() 写入警告框

   - 使用 document.write() 写入 HTML 输出

     **注意：**在 HTML 文档完全加载后使用 **document.write()** 将*删除所有已有的 HTML* ：

   - 使用 innerHTML 写入 HTML 元素

   - 使用 console.log() 写入浏览器控制台

#### 构造变量名称（唯一标识符）的通用规则是：

- 名称可包含字母、数字、下划线和美元符号
- 名称必须以字母开头
- 名称也可以 $ 和 _ 开头（但是在本教程中我们不会这么做）
- 名称对大小写敏感（y 和 Y 是不同的变量）
- 保留字（比如 JavaScript 的关键词）无法用作变量名称

## 变量以及运算符：

**声明变量之后，变量是没有值的。（技术上，它的值是 undefined）**

**重复声明 JavaScript 变量**

​        	如果再次声明某个 JavaScript 变量，将不会丢它的值。

​			在这两条语句执行后，变量 carName 的值仍然是 "porsche"**

```js
var carName = "porsche";
var carName; 
```

当字符串加上数值时，将会变成其余数值会被视作字符串并被**级联**。

例如var a = “8” + 3 + 5，其结果等于835。在用于字符串时，**+** 运算符被称为**级联运算符**。

**比较运算符：**

| 运算符  |        描述        |
| :-----: | :----------------: |
|   ==    |        等于        |
| **===** |    **等值等型**    |
|   !=    |       不相等       |
| **!==** | **不等值或不等型** |
|    >    |        大于        |
|    <    |        小于        |
|   >=    |     大于或等于     |
|   <=    |     小于或等于     |
|    ?    |     三元运算符     |

### JavaScript 类型运算符

| 运算符     | 描述                                  |
| :--------- | :------------------------------------ |
| typeof     | 返回变量的类型。                      |
| instanceof | 返回 true，如果对象是对象类型的实例。 |

运算符\*\*是幂运算 例如3\**2，结果是9

在js里面除法就是除法，例如7/2，结果是3.5，而不是3

### JavaScript 运算符优先级值

| 值   | 运算符     | 描述             | 实例             |
| :--- | :--------- | :--------------- | :--------------- |
| 20   | ( )        | 表达式分组       | (3 + 4)          |
|      |            |                  |                  |
| 19   | .          | 成员             | person.name      |
| 19   | []         | 成员             | person["name"]   |
| 19   | ()         | 函数调用         | myFunction()     |
| 19   | new        | 创建             | new Date()       |
|      |            |                  |                  |
| 17   | ++         | 后缀递增         | i++              |
| 17   | --         | 后缀递减         | i--              |
|      |            |                  |                  |
| 16   | ++         | 前缀递增         | ++i              |
| 16   | --         | 前缀递减         | --i              |
| 16   | !          | 逻辑否           | !(x==y)          |
| 16   | typeof     | 类型             | typeof x         |
|      |            |                  |                  |
| 15   | **         | 求幂 (ES7)       | 10 ** 2          |
|      |            |                  |                  |
| 14   | *          | 乘               | 10 * 5           |
| 14   | /          | 除               | 10 / 5           |
| 14   | %          | 模数除法         | 10 % 5           |
|      |            |                  |                  |
| 13   | +          | 加               | 10 + 5           |
| 13   | -          | 减               | 10 - 5           |
|      |            |                  |                  |
| 12   | <<         | 左位移           | x << 2           |
| 12   | >>         | 右位移           | x >> 2           |
| 12   | >>>        | 右位移（无符号） | x >>> 2          |
|      |            |                  |                  |
| 11   | <          | 小于             | x < y            |
| 11   | <=         | 小于或等于       | x <= y           |
| 11   | >          | 大于             | x > y            |
| 11   | >=         | 大于或等于       | x >= y           |
| 11   | in         | 对象中的属性     | "PI" in Math     |
| 11   | instanceof | 对象的实例       | instanceof Array |
|      |            |                  |                  |
| 10   | ==         | 相等             | x == y           |
| 10   | ===        | 严格相等         | x === y          |
| 10   | !=         | 不相等           | x != y           |
| 10   | !==        | 严格不相等       | x !== y          |
|      |            |                  |                  |
| 9    | &          | 按位与           | x & y            |
| 8    | ^          | 按位 XOR         | x ^ y            |
| 7    | \|         | 按位或           | x \| y           |
| 6    | &&         | 逻辑与           | x && y           |
| 5    | \|\|       | 逻辑否           | x \|\| y         |
| 4    | ? :        | 条件             | ? "Yes" : "No"   |
|      |            |                  |                  |
| 3    | =          | 赋值             | x = y            |
| 3    | +=         | 赋值             | x += y           |
| 3    | -=         | 赋值             | x -= y           |
| 3    | *=         | 赋值             | x *= y           |
| 3    | %=         | 赋值             | x %= y           |
| 3    | <<=        | 赋值             | x <<= y          |
| 3    | >>=        | 赋值             | x >>= y          |
| 3    | >>>=       | 赋值             | x >>>= y         |
| 3    | &=         | 赋值             | x &= y           |
| 3    | ^=         | 赋值             | x ^= y           |
| 3    | \|=        | 赋值             | x \|= y          |
|      |            |                  |                  |
| 2    | yield      | 暂停函数         | yield x          |
| 1    | ,          | 逗号             | 7 , 8            |

**提示：**括号中的表达式会在值在表达式的其余部分中被使用之前进行完全计算。

## javascript的数据类型：

**字符串值，数值，布尔值，数组，对象**

JavaScript 拥有动态类型。这意味着相同变量可用作不同类型：

```js
var x;               // 现在 x 是 undefined
var x = 7;           // 现在 x 是数值
var x = "Bill";      // 现在 x 是字符串值
```

### JavaScript 字符串值

字符串（或文本字符串）是一串字符（比如 "Bill Gates"）。

字符串被引号包围。您可使用单引号或双引号：

### JavaScript 数值

JavaScript 只有一种数值类型。

写数值时用不用小数点均可：

### JavaScript 布尔值

布尔值只有两个值：true 或 false。

### JavaScript 数组

JavaScript 数组用方括号书写。

数组的项目由逗号分隔。

下面的代码声明（创建）了名为 cars 的数组，包含三个项目（汽车品牌）：

```js
var cars = ["Porsche", "Volvo", "BMW"];	
```

数组索引基于零，这意味着第一个项目是 [0]，第二个项目是 [1]，以此类推。

### JavaScript 对象

JavaScript 对象用花括号来书写。

对象属性是 *name*:*value* 对，由逗号分隔。

```js
var person = {firstName:"Bill", lastName:"Gates", age:62, eyeColor:"blue"};
```

### Undefined

在 JavaScript 中，没有值的变量，其值是 undefined。typeof 也返回 undefined。

任何变量均可通过设置值为 undefined 进行清空。其类型也将是 undefined。

### Null

在 JavaScript 中，null 是 "nothing"。它被看做不存在的事物。

不幸的是，在 JavaScript 中，null 的数据类型是对象。

您可以把 null 在 JavaScript 中是对象理解为一个 bug。它本应是 null。

您可以通过设置值为 null 清空对象：

```
var person = null;           // 值是 null，但是类型仍然是对象
```

#### Undefined 与 Null 的区别

Undefined 与 null 的**值相等**，但类型不相等：

```
typeof undefined              // undefined
typeof null                   // object
null === undefined            // false
null == undefined             // true
```

### typeof 的用法

可通过typeof来确定数据的类型，不用加小括号，使用方法

```js
typeof 0   			     //输出结果为number
typeof "bill" 		     //输出结果为string
typeof [1,2,3] 			 //输出结果为object，因为js里数组属于对象
```

typeof 运算符可返回以下原始类型之一：

- string
- number
- boolean
- undefined
- function
- object

typeof 运算符把对象、数组或 null 返回 object。

typeof 运算符不会把函数返回 object。

```js
typeof {name:'Bill', age:62} // 返回 "object"
typeof [1,2,3,4]             // 返回 "object" (并非 "array"，参见下面的注释)
typeof null                  // 返回 "object"
typeof function myFunc(){}   // 返回 "function"
```

JavaScript里面的对象，一般意义上指的是用花括号括起来的键值对，但有两种特例，1.数组 2.null 

结束时间：00:33

----

## Day 2开始时间21:08

## JavaScript函数

使用上面的例子，toCelsius 引用的是函数对象，而 toCelsius() 引用的是函数结果

function toCelsius(f) {
    return (5/9) * (f-32);
}
document.getElementById("demo").innerHTML = toCelsius(86);

document.getElementById("demo").innerHTML = toCelsius;

// 第二种显示的就是toCelsius函数本身

### 局部变量

在 JavaScript 函数中声明的变量，会成为函数的*局部变量*。

局部变量只能在函数内访问。

```js
// 此处的代码不能使用 carName

function myFunction() {
    var carName = "Volvo";
    // code here CAN use carName
}

// 此处的代码可以使用 carName
```

由于局部变量只能被其函数识别，因此可以在不同函数中使用相同名称的变量。

局部变量在函数开始时创建，在函数完成时被删除。

## JavaScript对象详解

对象一般意义上指的是花括号括起来的键值对，键和值之间用冒号隔开，例如 var car = {type : "porsche", color : "white" }

### 对象方法

对象也可以有**方法**。方法是在对象上执行的**动作**。方法以*函数定义*被存储在属性中。

| 属性      | 属性值                                                    |
| :-------- | :-------------------------------------------------------- |
| firstName | Bill                                                      |
| lastName  | Gates                                                     |
| age       | 62                                                        |
| eyeColor  | blue                                                      |
| fullName  | function() {return this.firstName + " " + this.lastName;} |

方法是作为属性来存储的函数。

### this 关键词

在函数定义中，this 引用该函数的“拥有者”。

在上面的例子中，this 指的是“拥有” fullName 函数的 *person 对象*。

换言之，this.firstName 的意思是 *this 对象*的 firstName 属性。

```js
var person = {
  firstName: "Bill",
  lastName : "Gates",
  id       : 678,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
```

### 访问对象属性

您能够以两种方式访问属性：

```
objectName.propertyName
```

或者

```
objectName["propertyName"]
```

所以现在对于 数组是一种对象，是不是能够理解了呢，数组其实就是键值对，只不过键是0到n的数字而已。

如果通过关键词 "new" 来声明 JavaScript 变量，则该变量会被创建为对象：

```
var x = new String();        // 把 x 声明为 String 对象
var y = new Number();        // 把 y 声明为 Number 对象
var z = new Boolean();       //	把 z 声明为 Boolean 对象
```

请避免字符串、数值或逻辑对象。他们会增加代码的复杂性并降低执行速度。

结束时间21:41

## JS事件

| onchange    | HTML 元素已被改变            |
| ----------- | ---------------------------- |
| onclick     | 用户点击了 HTML 元素         |
| onmouseover | 用户把鼠标移动到 HTML 元素上 |
| onmouseout  | 用户把鼠标移开 HTML 元素     |
| onkeydown   | 用户按下键盘按键             |
| onload      | 浏览器已经完成页面加载       |

## JS字符串详解

字符串可以通过单引号或者双引号

```js
var carname = "Porsche 911";
var carname = 'Porsche 911';
```

字符串的长度可以通过 str.length 方法获取

```js
var txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
var sln = txt.length;
```

避免字符串的误解，可以使用反斜杠转义字符

| 代码 | 结果 | 描述   |
| :--- | :--- | :----- |
| \'   | '    | 单引号 |
| \"   | "    | 双引号 |
| \\   | \    | 反斜杠 |

### 长代码行换行

为了最佳可读性， 程序员们通常会避免每行代码超过 80 个字符串。

#### 如果某条 JavaScript 语句不适合一整行，那么最佳换行位置是某个运算符之后：

```js
document.getElementById("demo").innerHTML =
"Hello Kitty.";
```

#### 您也可以*在字符串中*换行，通过一个反斜杠即可：

```js
document.getElementById("demo").innerHTML = "Hello \
Kitty!";
```

**部分浏览器不支持**

对长字符串换行的最安全做法（但是有点慢）是使用字符串加法：

```js
document.getElementById("demo").innerHTML = "Hello" + 
"Kitty!";
```

您不能通过反斜杠对代码行进行换行：

```js
document.getElementById("demo").innerHTML = \ 
"Hello Kitty!";
```

## 字符串可以是对象

通常，JavaScript 字符串是原始值，通过字面方式创建：

```js
var firstName = "Bill"
```

但是字符串也可通过关键词 new 定义为对象：

```js
var firstName = new String("Bill")
```

#### js中两个对象无法比较

```js
var x = new String("Bill");             
var y = new String("Bill");

// (x == y) 为 false，因为 x 和 y 是不同的对象
// (x === y) 为 false，因为 x 和 y 是不同的对象
// 两个对象进行比较，返回值必定为false
```

### 字符串方法：

字符串是一种原样保持的数据结构，无论输入多少空格它都会保留下来。

##### str.length  //返回字符串长度

从前往后检索

##### str.indexof("china") //返回字符串在str中首次出现的索引

从后往前检索

##### str.lastIndexOf() //返回字符串在str中最后出现的缩影

indexof 和lastIndexOf 如果未找到文本，均返回-1

两种方法都接受作为检索起始位置的第二个参数。

```js
var str = "The full name of China is the People's Republic of China.";
var pos = str.indexOf("China", 18);
```

lastIndexOf() 方法向后进行检索（从尾到头），这意味着：假如第二个参数是 50，则从位置 50 开始检索，直到字符串的起点。

```js
var str = "The full name of China is the People's Republic of China.";
var pos = str.lastIndexOf("China", 50);
```

## 检索字符串中的字符串

search() 方法搜索特定值的字符串，并返回匹配的位置：

```js
var str = "The full name of China is the People's Republic of China.";
var pos = str.search("locate");
```

两种方法，indexOf() 与 search()，是*相等的*。

这两种方法是不相等的。区别在于：

- search() 方法无法设置开始位置参数。
- indexOf() 方法无法设置更强大的搜索值（正则表达式）。

## 提取部分字符串

有三种提取部分字符串的方法：

- slice(*start*, *end*)
- substring(*start*, *end*)
- substr(*start*, *length*)

### slice方法

设置的是两个参数：起始索引（开始位置），终止索引（结束位置），当某个参数为负，则从字符串的结尾开始计数。如果当某个参数为负，则从字符串的结尾开始计数。

```js
var str = "Apple, Banana, Mango";
var res = str.slice(-13,-7);
```

当slice参数为负数时，也是第一个参数一定比第二个参数小

如果省略第二个参数，默认裁剪剩余部分。

本质上获取的长度是 [起始索引，终止索引)  左闭右开

### substring方法

类似于slice方法，不同点在于substring无法接受负的数字

### substr方法

不同之处在于第二个参数规定被提取部分的长度

```js
var str = "Apple, Banana, Mango";
var res = str.substr(7,6);
```

## 替换字符串内容

replace() 方法用另一个值替换在字符串中指定的值：

```js
str = "Please visit Microsoft!";
var n = str.replace("Microsoft", "W3School");
```

replace() 方法不会改变调用它的字符串。它返回的是新字符串。

默认地，replace() *只替换首个匹配*：

默认地，replace() 对大小写敏感。因此不对匹配 MICROSOFT：

如需执行大小写不敏感的替换，请使用正则表达式 /i（大小写不敏感）：

```js
str = "Please visit Microsoft!";
var n = str.replace(/MICROSOFT/i, "W3School");
```

如需替换所有匹配，请使用正则表达式的 g 标志（用于全局搜索）：

```js
str = "Please visit Microsoft and Microsoft!";
var n = str.replace(/Microsoft/g, "W3School");
```

### concat() 方法

concat() 连接两个或多个字符串：

```js
var text1 = "Hello";
var text2 = "World";
text3 = text1.concat(" ",text2);
```

concat() 方法可用于代替加运算符。下面两行是等效的：

```js
var text = "Hello" + " " + "World!";
var text = "Hello".concat(" ","World!");
```

所有字符串方法都会返回新字符串。它们不会修改原始字符串。

正式地说：字符串是不可变的：字符串不能更改，只能替换。

### string.trim()方法

删除字符串两端的空白符

```js
var str = "       Hello World!        ";
alert(str.trim());
```

## 提取字符串字符

这是两个提取字符串字符的*安全*方法：

- charAt(*position*)
- charCodeAt(*position*)

charAt() 方法返回字符串中指定下标（位置）的字符串：

charCodeAt() 方法返回字符串中指定索引的字符 unicode 编码：

```js
var str = "HELLO WORLD";

str.charCodeAt(0);         // 返回 72
```

同时也支持属性访问

```
var str = "HELLO WORLD";
str[0];                   // 返回 H
```

使用属性访问有点不太靠谱：

- 不适用 Internet Explorer 7 或更早的版本
- 它让字符串看起来像是数组（其实并不是）
- 如果找不到字符，[ ] 返回 undefined，而 charAt() 返回空字符串。
- 它是只读的。str[0] = "A" 不会产生错误（但也不会工作！）//意思是它是不可写的。

```js
var str = "HELLO WORLD";
str[0] = "A";             // 不产生错误，但不会工作
str[0];                   // 返回 H
```

## 字符串转换成数组

split方法将字符串转换成数组;

```js
var txt = "a,b,c,d,e";   // 字符串
txt.split(",");          // 用逗号分隔
txt.split(" ");          // 用空格分隔
txt.split("|");          // 用竖线分隔
```

如果省略分隔符，被返回的数组将包含 index [0] 中的整个字符串。

// 意思是 str[0] 里面包含原来的所有字符串 str[1]为undefined

如果分隔符是 ""，被返回的数组将是间隔单个字符的数组：

## JavaScript 数字

**JavaScript 只有一种数值类型。**

**JavaScript 数值始终是 64 位的浮点数**

整数（不使用指数或科学计数法）会被精确到 15 位。

```
var x = 999999999999999;   // x 将是 999999999999999
var y = 9999999999999999;  // y 将是 10000000000000000
```

小数的最大数是 17 位，但是浮点的算数并不总是 100% 精准：

```js
var x = 0.2 + 0.1;         // x 将是 0.30000000000000004
```

```js
var x = (0.2 * 10 + 0.1 * 10) / 10;       // x 将是 0.3
```

在进行数字运算时 js 会尝试将字符串转换成数字

```
var x = "100";
var y = "10";
var z = x / y;       // z 将是 10
```

但是加法除外， 加法时级联运算

## NaN - 非数值

NaN 属于 JavaScript 保留词，指示某个数不是合法数。

尝试用一个非数字字符串进行除法会得到 NaN（Not a Number）：

```
var x = 100 / "Apple";  // x 将是 NaN（Not a Number）
```

#### isNaN函数可以测出变量是否是数字

NaN 是数，typeof NaN 返回 number：

```js
typeof NaN;             // 返回 "number"
```

## Infinity

Infinity （或 -Infinity）是 JavaScript 在计算数时超出最大可能数范围时返回的值。

除以 0（零）也会生成 Infinity：

```js
var x =  2 / 0;          // x 将是 Infinity
var y = -2 / 0;          // y 将是 -Infinity
```

Infinity 是数：typeOf Infinity 返回 number。

```js
typeof Infinity;        // 返回 "number"
```

但是您能够使用 toString() 方法把数输出为十六进制、八进制或二进制。

```js
var myNumber = 128;
myNumber.toString(16);     // 返回 80
myNumber.toString(8);      // 返回 200
myNumber.toString(2);      // 返回 10000000
```

