# hpc-learning

first repository

## 我想做什么

- 走完超算队考核任务，掌握 Git/GitHub、Linux 终端等基本工具
- 记录学习笔记、实验代码和踩过的坑
- 长期方向：AIGC / 虚拟数字人 / 游戏开发，希望把 HPC 与图形学的基础打牢

## 目前环境

- 设备：MacBook Pro (M5 Pro / 48GB)
- 系统：macOS
- Git：2.54.0（Apple 自带版本）
- 终端：zsh
- Python：3.9.6（系统自带，**课程代码零第三方依赖**）

## 项目结构

```
hpc/            迷你 HPC 工具箱（纯标准库）
  partition.py    分块归约：切分 -> 局部计算 -> 合并
  schedule.py     任务调度：轮询 / 贪心 LPT / makespan
  matmul.py       矩阵乘：朴素 / 分块 / C 层点积
  histogram.py    并行直方图：局部计数 + 合并
  perf.py         性能模型：加速比 / 效率 / Amdahl / roofline
  cli.py          演示入口
tests/          76 个行为测试（unittest）
```

## 怎样运行项目

跑演示（约 1 秒，打印五组可观察的测量）：

```bash
python3 -m hpc
```

跑全部测试：

```bash
python3 -m unittest discover -s tests -v
```

无需 pip install，也无需虚拟环境。

## 课程

本仓库由 ProMentor 生成了配套源码课程（`.promentor/`）：

```bash
/promentor            # 查看课程面板与进度
/promentor learn ch01 # 开始第一章
/promentor test       # 跑当前章 Lab 测试
```
- 2026-10-21：完成首次本地 commit/push，Task1 全流程闭环
