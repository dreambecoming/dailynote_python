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
