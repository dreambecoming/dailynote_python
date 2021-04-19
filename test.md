1. f-string 格式化字符串常量（formatted string literals）

* 获取当前时间
```python
from datetime import datetime
e = datetime.now()
f'the time is {e:%F %X}'
```

2. nvidia-smi
显示所有GPU的当前信息状态。System management interface

watch -n 0.1 nvidia-smi 每0.1秒刷新
https://blog.csdn.net/handsome_bear/article/details/80903477

3. random.choice( seq ) 返回一个列表，元组或字符串的随机项

4. os.walk(top[, topdown=True[, onerror=None[, followlinks=False]]])
https://www.runoob.com/python/os-walk.html
```python
def walkFile(file):
    for root, dirs, files in os.walk(file):

        # root 表示当前正在访问的文件夹路径
        # dirs 表示该文件夹下的子目录名list
        # files 表示该文件夹下的文件list

        # 遍历文件
        for f in files:
            print(os.path.join(root, f))

        # 遍历所有的文件夹
        for d in dirs:
            print(os.path.join(root, d))
  ```
5. URL（Uniform Resource Locator）：统一资源定位符 "协议://IP地址/路径和文件名
URI（Universal Resource Identifier）：统一资源标识符  
URN（Uniform Resource Name）：统一资源名称  
* URI 包含 URL or URN 
* Data URI scheme 简称 Data URI  
https://blog.csdn.net/qq_38128179/article/details/100663085

7. ％05d和％5d

%nd 输出的整型宽度至少为n位，右对齐，%5d即宽度至少为5位，位数大于5则输出实际位数  
%0nd 用得比较多，表示输出的整型宽度至少为n位，不足n位用0填充  
printf（"%05d",1）输出：00001  
printf（"%5d",1）输出：****1（*为空格）  

8. 字符串
* Python 将一个列表里面的元素拼接成一个字符串
```python
    item1 = ["lowman", "isbusy"]
    item2 = ",".join(item1) # 根据实际需要使用相应的分隔符连接列表元素,如 , : ; 或者空字符串
    print(item2)
    print(type(item2)) # 输出:  "lowman,isbusy"
```
  删除字符串中连续多个空格并保留一个 str=' '.join(line.split())
* 判断字符串是否为空
    len(a)>0
    a.strip()==''
    a.isspace() == True

9. 字典

* locals() globals()

'键-值对' 转为 '变量-变量值对'
```python
# https://blog.csdn.net/nyan_pass/article/details/80102308
dictA={'key1':'value1','key2':'value2','key3':'value3'}
globals().update(dictA) # 将 dictA 添加到 全局变量中
print(key1,key2,key3)
```
* 值反查键
https://blog.csdn.net/edians/article/details/99296269
```python
mydisc = {'key1':'123', 'key2':'234', 'key3':'345','key5':'123'}
get_value = input('请输入要查值：')
if get_value in mydisc.values():
    for a in range(0,len(mydisc)):
        if list(mydisc.values())[a]==get_value:
            print(list(mydisc.keys())[a])
else:
    print('你要查询的值'+get_value+'不存在')
```

10. 符号

* *、** 号
调用函数 和 定义函数 时候   
https://blog.csdn.net/yhs_cy/article/details/79438706  
https://www.cnblogs.com/omg-hxy/p/9081177.html
```python
def F(*args):
    print(args)

F('XVID')
F(*'XVID')
print(*'XVID')
print(*['X','V','I','D'])
#输出
# ('XVID',)
# ('X', 'V', 'I', 'D')
# X V I D
# X V I D
```
* // 除法向下取整


10. 查找匹配 文件名  
```python
import os
 
pathlog = "/usr/local/nginx/log"
files = os.listdir(pathlog)
for f in files:
    if 'stat' in f and f.endswith('.log'):
```
