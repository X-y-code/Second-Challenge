# Second-Challenge

## 一、环境信息

| 项目 | 版本 |
|------|------|
| GPU | NVIDIA GeForce RTX 5060 (8GB) |
| 操作系统 | Windows 11 + WSL2 Ubuntu 22.04 |
| CUDA Version | 13.1 |
| Python | 3.10 |
| SGLang | 0.5.14 |
| Ray | 2.56.0 |
| 模型 | Qwen/Qwen3-0.6B |


## 二、安装方法

### 1. 创建虚拟环境

```bash
python3 -m venv sglang
source sglang/bin/activate
```


### 2. 安装依赖

\`\`\`bash
uv pip install sglang==0.5.14 ray==2.56.0
uv pip install requests numpy
\`\`\`


## 三、启动命令

\`\`\`bash
source /mnt/c/Users/20798/sglang/bin/activate

python3 -m sglang.launch_server \
  --model-path Qwen/Qwen3-0.6B \
  --host 0.0.0.0 \
  --port 30000 \
  --page-size 64 \
  --attention-backend triton \
  --disable-cuda-graph \
  --enable-cache-report
\`\`\`

## 四、回放命令

\`\`\`bash
cd /mnt/d/Chall
python task1_measure.py
\`\`\`
