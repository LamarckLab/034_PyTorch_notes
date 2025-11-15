<h1 align="center">🧬 Dive into Deep Learning 笔记</h1>

<p align="center">
  <i> —— 2025.11.15</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-blue?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Framework-PyTorch-orange?logo=pytorch" />
  <img src="https://img.shields.io/badge/Platform-Linux-lightgrey?logo=linux" />
  <img src="https://img.shields.io/badge/Status-Complete-brightgreen" />
</p>

---

## 🧪 Environment Configuration

```bash
# 开发环境配置在236 server上 (这台机子的CUDA Version:12.2)
# 创建lmk_AI环境
conda create -n lmk_AI python=3.10 -y
# 安装GPU版的PyTorch
python -m pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
# 给lmk_AI环境安装Jupyter的Python内核（ipykernel包）
python -m pip install ipykernel
# 把lmk_AI这个conda环境注册成一个Jupyter可选内核，名字叫“LMK AI (GPU)”
python -m ipykernel install --user --name lmk_AI --display-name "LMK AI (GPU)"
# 安装Jupyter Lab
python -m pip install jupyterlab
```

