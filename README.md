# ECS资源初始化系统指南

在申请了ECS算力资源后，需要对ECS进行初始化操作，才能正式投入工作
初始化内容主要包含以下几点:
1. 更新默认的DNS信息，这样才能访问互联网
2. 更新默认的镜像源信息，这样才能安装所需软件
3. 默认ECS资源采用系统盘和数据盘分离创建方式，所以需要格式化你的数据盘，并进行挂载后才能使用
4. 以上内容均可通过"system-init"工具实现。具体操作请往下看。


## 初始化步骤
### 1. 下载"system-init"工具
```
wget http://shunxiang.oss-cn-jswx-xuelang-d01-a.ops.cloud.wuxi-yqgcy.cn/system-init.sh
```

### 2. 更新DNS信息
```
system-init.sh --dnsinit
```

### 3. 配置Yum源信息
```
system-init.sh --repoinit
```

### 4. 数据盘格式化并挂载
```
system-init.sh --diskinit
```


