---
title: 安装CUDA和PyTorch
date: 2025-06-16
categories: [research, discussion]
tags: [discussion]
toc:  true
---

# 安装CUDA
CUDA是NVIDIA提供的并行计算平台和编程模型，允许开发者使用GPU进行通用计算。安装CUDA通常需要以下步骤：
1. **检查系统兼容性**：在cmd中输入`nvidia-smi`  如果能运行，说明驱动已安装。右上角是CUDA版本
2. **下载CUDA Toolkit**：访问[NVIDIA CUDA Toolkit下载页面](https://developer.nvidia.com/cuda-downloads)，选择你的操作系统和版本，下载相应的安装包。
3. **安装CUDA Toolkit**：运行下载的安装包，按照提示进行安装。通常会包括驱动程序、编译器和库文件等。
   - 选自定义安装，在CUDA中，取消调Visual Studio Integration的选项，因为它可能会导致一些兼容性问题。
4. **设置环境变量**：安装完成后，需要将CUDA的bin目录添加到系统的PATH环境变量中，以便在命令行中使用CUDA工具。
5. **验证安装**：可以通过运行`nvcc --version`命令来检查CUDA是否安装成功。如果显示CUDA版本信息，则表示安装成功。

# 安装PyTorch
PyTorch是一个流行的深度学习框架，支持GPU加速。安装PyTorch通常需要以下步骤：
1. **检查CUDA版本**：确保你的CUDA版本与PyTorch兼容。可以在[PyTorch官网](https://pytorch.org/get-started/locally/)上查看兼容性表。
2. **选择安装方式**：PyTorch可以通过pip或conda安装。根据你的环境选择合适的安装方式。
3. **使用pip安装**：在命令行中输入以下命令（根据你的CUDA版本选择合适的命令）：
   ```bash
   pip install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu118
   ```
   这里的`cu118`表示CUDA 11.8版本，如果你使用的是其他版本，请替换为相应的版本号。
4. **验证安装**
   安装完成后，可以通过以下代码验证PyTorch是否能够正确使用CUDA：
   ```python
   import torch
   print("CUDA available:", torch.cuda.is_available())
   print("CUDA version:", torch.version.cuda)
   print("PyTorch version:", torch.__version__)
   ```  
---


---

Want to see something else added? <a href="https://github.com/MingshuoXu/MingshuoXu.github.io/issues/new">Open an issue.</a>

[^fn-sample_footnote]: Handy! Now click the return link to go back.
