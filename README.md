# MLP-XOR-Lab · 个人网站与心情实验室

课程作业展示站，参照以下三个页面的风格与内容组织方式制作：

1. https://hugohe8380.github.io/XOR-MLP-Visualizer/
2. https://alphekka221.github.io/myweb/MLP.html
3. https://tiantian-site-d4g3fg87d2be77723-1509113181.tcloudbaseapp.com/mood-lab-20261115/

## 页面

- `index.html` — 个人主页（01 首页 / 02 关于 / 03 AI 作品 / 04 小确幸 / 05 动态 / 06 留言 / 07 心情实验室入口）
  - 音乐播放器使用 Web Audio 合成旋律，无外部音频文件
  - 相册为 SVG 占位内容，可替换为真实图片
  - 动态与留言使用浏览器 localStorage 存储；管理员密码为演示用 `mlp2026`
- `mlp.html` — MLP 心情实验室（XOR 参数学习可视化）
  - 浏览器本地用 JavaScript 训练一个 2→2→1 多层感知机（sigmoid + BCE + Adam，全批量）
  - 固定随机种子，稳定收敛到 XOR：预测 `[0, 1, 1, 0]`，损失约 0.00002
  - 支持：权重连线可视化、样本逐步计算、训练轮次拖动/播放、Loss/Accuracy 指标、损失曲线、决策区域与阈值滑块、PyTorch/TensorFlow 工作流对照
  - 单文件、无后端、无外部依赖
- `styles.css` — 共享样式（纸感/杂志风，暖白背景 + 墨色文字 + 陶土色强调）

## 本地预览

```bash
python -m http.server 8899
# 打开 http://localhost:8899/
```

## 部署

纯静态站点，可直接部署到 GitHub Pages / CloudBase / 任意静态托管。把整个目录内容提交到仓库根即可。
