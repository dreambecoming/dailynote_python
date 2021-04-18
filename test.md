1. f-string 获取当前时间

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

6. // 除法向下取整

7. cd（change directory）
cd / 跳转根目录  
cd ../  跳转上一级目录 "/"可省略  
cd 、cd ~ 和cd $HOME  跳转到当前用户的家目录  
cd - 跳转进入此目录之前所在目录

8. ％05d和％5d

%nd 输出的整型宽度至少为n位，右对齐，%5d即宽度至少为5位，位数大于5则输出实际位数  
%0nd 用得比较多，表示输出的整型宽度至少为n位，不足n位用0填充  
printf（"%05d",1）输出：00001  
printf（"%5d",1）输出：****1（*为空格）  
