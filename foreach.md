## 数组练习
在一个大学的编程选修课班里，我们得到了一组参加该班级的学生数据，分别是姓名、性别、年龄和年级，接下来呢，我们要利用JavaScript的知识挑出其中所有是大一的女生的的名字哦。
学生信息如下：
 ```javascript
    ('小A','女',21,'大一'),  ('小B','男',23,'大三'),
    ('小C','男',24,'大四'),  ('小D','女',21,'大一'),
    ('小E','女',22,'大四'),  ('小F','男',21,'大一'),
    ('小G','女',22,'大二'),  ('小H','女',20,'大三'),
    ('小I','女',20,'大一'),  ('小J','男',20,'大三')
 ```

### 任务
第一步： 把这些数据组成一个数组，方便我们之后操作哦。
提示: 使用二维数组。
第二步： 筛选数据吧，首先找出都是大一的所有信息 ;
第三步： 最后再一次筛选上一步得到的数据，打印出都是女生的姓名 ;
提示: 可以用switch 或 if 语句进行筛选。

### 代码
```html
<!DOCTYPE  HTML>
<html >
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>流程控制语句</title>
<script type="text/javascript">
//第一步把之前的数据写成一个数组的形式,定义变量为 infos
var infos=[["小A","女",21,"大一"],
["小B","男",23,"大三"],
["小C","男",24,"大四"],
["小D","女",21,"大一"],
["小E","女",22,"大四"],
["小F","男",21,"大一"],
["小G","女",22,"大二"],
["小H","女",20,"大三"],
["小I","女",20,"大一"],
["小J","男",20,"大三"]];
//第一次筛选，找出都是大一的信息
//第二次筛选，找出都是女生的信息

/*方法一：进阶版！！
var dayis = []
dayis = infos.filter((infoItem) =>{
return infoItem.indexOf('大一') > -1 && infoItem.indexOf('女') > -1
      })
console.log(dayis)
var females = dayis.map(dayi => dayi[0])
console.log(females)
document.write(females.join(''))
console.log(females.join("-"))

方法二：高级版！！！
infos.forEach((item) => {
    if (item[3] === '大一' && item[1] === '女') {
        document.write(item[0] + ' ')
    }
})
初级版以下·
*/
for(var i=1;i++;i<infos.length){
   if(infos[i][3]==='' &&infos[i][1]===''){
      document.write(infos[i][0]);
   }
}

</script>
</head>
<body>
</body>
</html>
```

### 效果
![](./image/Snipaste_2017-09-07_22-57-03.png)