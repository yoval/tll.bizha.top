# Conda 的使用

---

### 环境

- np1_env

`conda create -n np1_env python=3.9`

用于运行 cpca 相关代码。


### 创建 Conda 环境

- 创建新 Conda 环境

```bash
conda create -n tll python=3.7
```

- 激活 Conda 环境

```bash
conda activate tll
```

- 退出 Conda 环境

```bash
conda deactivate
```

### 管理环境

- 查看所有环境

```bash
conda env list
``` 

- 删除环境

```bash
conda env remove -n tll
```

### 安装软件包

- 在当前环境下安装软件包

```bash
conda install -n tll pandas
```

- 在指定环境下安装软件包

```bash
conda install -n tll pandas
```

### 导出和导入环境配置

- 导出环境配置

锁定版本号

```bash
conda env export  > environment.yml
```

不锁定版本号

```bash
conda env export --no-builds > environment.yml
```

- 导入环境配置

```bash
conda env create -f environment.yml
```

### 使用国内镜像源加速下载

- 添加阿里云镜像源

```bash
conda config --add channels https://mirrors.aliyun.com/anaconda/pkgs/main/
conda config --add channels https://mirrors.aliyun.com/anaconda/pkgs/free/
conda config --set show_channel_urls yes
```

