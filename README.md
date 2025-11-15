<h1 align="center">🧬 《动手学深度学习》笔记</h1>

<p align="center">
  <i> —— 2025.11.15</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-blue?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Framework-PyTorch-orange?logo=pytorch" />
  <img src="https://img.shields.io/badge/Platform-Linux-lightgrey?logo=linux" />
  <img src="https://img.shields.io/badge/Status-In%20Progress-yellow" />
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
# 运行Jupyter Lab
jupyter lab --no-browser --port=8899
```

## 🔐 SSH Port Forwarding（访问远程 Jupyter Lab）

远程服务器上的 Jupyter Lab 默认只监听本机（`127.0.0.1`），无法从外部直接访问。  
因此需要通过 **SSH 本地端口转发（SSH Tunnel）** 将服务器的端口映射到本地电脑。

---

```bash
# 在本地终端创建端口转发
ssh -L 8899:127.0.0.1:8899 amax@192.168.208.236
# 在端口转发保持开启的情况下，打开浏览器访访问 (本地和服务器的session都要保持连接)
http://localhost:8899
# 随后进入服务器端的Jupyter Lab（首次需要输入token）
```

## 启动！！！
```
# server上运行Jupyter Lab
jupyter lab --no-browser --port=8899
# 在本地终端创建端口转发
ssh -L 8899:127.0.0.1:8899 amax@192.168.208.236
# 浏览器访问
http://localhost:8899
```
