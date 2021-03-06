Java标准流程结构

![image-20200619180146882](http://imgbed-xia-2.oss-cn-hangzhou.aliyuncs.com/img/image-20200619180146882.png)

### 注释分类

- 单行注释

```
//
```



- 多行注释

```
/*
*/
```



- 文档注释

```
/**
*
*/
```

文档注释和多行的区别在于，在生成javadoc文件的时候，文档注释会出现在doc文件里面，而多行注释不会。

### 标识符

- 标识符：
  - Java 对各种**变量**、**方法**和**类**等要素命名时使用的字符序列称为标识符
  - **凡是自己可以起名字的地方都叫标识符**。

- 定义合法标识符规则：
  - **由26个英文字母大小写，0-9 **，_ **，$组成
  - **数字不可以开头。**
  - **不可以使用关键字和保留字，但能包含关键字和保留字。**
  - **Java**中严格区分大小写，长度无限制。
  - **标识符不能包含空格。**

l注意：在起名字时，为了提高阅读性，要尽量有意义，“见名知意”。