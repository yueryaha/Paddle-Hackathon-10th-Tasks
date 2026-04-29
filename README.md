# 飞桨第十期黑客松 - 打卡与进阶任务记录
**作者：** yueryaha | **赛道：** 文心合作伙伴赛道

## 📌 任务 1：Intel OpenVINO Notebook 快速上手打卡
* **硬件环境：** Windows / Intel CPU
* **软件环境：** Python 3.13 / OpenVINO 2026.1.0 / PaddleOCR-VL-1.5
* **核心成果：** 成功在本地 CPU 环境下完成模型的 INT8 压缩，并跑通图文 OCR 推理。
* **证明材料：**
    * [运行代码与完整日志](./paddleocr-vl.ipynb)
    * 截图 1：依赖安装成功
      ![依赖安装](./images/Environment.png)
    * 截图 2：模型转换为 OpenVINO 格式成功
      ![模型转换](./images/transform.png)
    * 截图 3：推理结果输出
      ![推理结果](./images/infer.png)

⚠️ 环境注记：
本次环境使用了最新的 Python 3.13。在运行最后的 Gradio 交互式 Demo 时，由于 Python 3.13 原生移除了 audioop 模块，导致 Gradio 内部依赖报错。虽然通过补充安装 audioop-lts 解决了模块缺失，但由于环境底层渲染机制问题，Demo 页面未能成功拉起。

结论： 核心的 OpenVINO IR 模型转换与端到端 OCR 推理均已在后台稳定执行完毕并成功输出结构化结果，证明核心推理流水线验证通过。
