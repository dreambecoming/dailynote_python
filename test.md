1. f-string 获取当前时间

```python
from datetime import datetime
e = datetime.now()
f'the time is {e:%F %X}'
```

2.nvidia-smi
显示所有GPU的当前信息状态。System management interface

watch -n 0.1 nvidia-smi 每0.1秒刷新
https://blog.csdn.net/handsome_bear/article/details/80903477
