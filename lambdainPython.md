`lambda`函数的用法
---
# `lambda argument_list: expression` 
1. `lamda`函数是匿名的，即`lambda`函数没有明字
2. `lambda`函数有输入和输出，输入是传入参数列表，输出是根据表达式计算得到的值
3. `lambda`函数的功能应该比较简单  
---
## 几个例子
1. `lambda x,y: x * y`,输入为x,y；输出为他们的积x*y
2. `lambda:None`,函数没有输入参数，输出为`None`
3. `lambda *args:sum(args)`,输入为任意个参数，输出它们的和

---
## 四种用法
1. 将`lambda`函数赋给一个变量，通过该变量间接调用该`lambda`函数
2. 将`lambda`函数作为其他函数的返回值
3. 将`lambda`函数赋给其他函数，从而用`lambda`函数替换掉该函数
4. **将`lambda`函数作为参数传递给其他函数**  


    4.1 `filter`函数：`filter(lambda x:x % 3 == 0,[1,2,3])`，将列表[1,2,3]中能够被3整除的元素过滤出来
    4.2 `sorted`函数：`sorted([1,2,3,4,5,6,7,8,9],key = lambda x : abs(5 - x))`，将列表[1,2,3,4,5,6,7,8,9]中的元素按照与5的距离从小到大排列 
    4.3 `map`函数：`map(lambda x : x+1,[1,2,3])`，将列表[1,2,3]中每个元素加1
    4.4 `reduce`函数：`reduce(lambda a,b : '{},{}'.format(a,b),[1,2,3,4,5,6])`,具体执行为：1,2 -> '1,2' ; '1,2',3 -> '1,2,3'; '1,2,3',4 -> '1,2,3,4' ;直到整个列表变为'1,2,3,4,5,6'
     