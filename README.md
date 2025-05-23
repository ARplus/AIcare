# AIcare
💗 基于WebRTC的非接触式心率检测 | AI护工项目的心率监测模块 | 使用摄像头实时检测心率 | Browser-based Heart Rate Detection using Photoplethysmography (PPG)
# 💗 AI护工 - 心率检测系统

<p align="center">
  <img src="https://img.shields.io/badge/WebRTC-Enabled-brightgreen" alt="WebRTC">
  <img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License">
  <img src="https://img.shields.io/badge/PRs-Welcome-brightgreen.svg" alt="PRs Welcome">
</p>

一个基于浏览器的非接触式心率检测应用，使用摄像头和光电容积脉搏波（PPG）技术实时监测心率，无需任何可穿戴设备。

## 🌟 在线演示

🔗 [在线体验地址](https://ARplus.github.io/heart-rate-detector/)

## ✨ 功能特点

- 🎥 **非接触式检测** - 仅使用普通摄像头，无需额外硬件
- 📱 **跨平台支持** - 支持PC和移动设备
- 🔒 **隐私安全** - 所有处理均在本地完成，不上传任何数据
- 📊 **实时显示** - 动态波形图和心率数值实时更新
- ⏱️ **自动检测** - 30秒自动完成检测并显示结果
- 🌐 **纯前端实现** - 无需后端服务器

## 🚀 快速开始

### 在线使用

1. 使用支持WebRTC的现代浏览器访问演示地址
2. 点击"开始检测"按钮
3. 允许浏览器访问摄像头
4. 将面部对准屏幕上的虚线框
5. 保持静止30秒，等待检测完成

### 本地部署

```bash
# 克隆项目
git clone https://github.com/your-username/heart-rate-detector.git

# 进入项目目录
cd heart-rate-detector

# 使用任意HTTP服务器运行（需要HTTPS或localhost）
# 方式1：使用Python
python -m http.server 8000

# 方式2：使用Node.js的http-server
npx http-server

# 方式3：使用VS Code的Live Server插件
```

然后在浏览器中访问 `http://localhost:8000`

## 🔬 技术原理

本项目基于**光电容积脉搏波描记法（Photoplethysmography, PPG）**原理：

1. **血液光学特性**：血液中的血红蛋白对绿光的吸收率会随心跳变化
2. **信号采集**：通过摄像头捕获面部（主要是前额）的视频流
3. **颜色分析**：提取每帧图像中绿色通道的平均值
4. **信号处理**：
   - 去除基线漂移
   - 带通滤波（0.75-3Hz）
   - 峰值检测
5. **心率计算**：通过分析峰值间隔计算每分钟心跳数（BPM）

## 💻 技术栈

- **WebRTC** - 摄像头访问和视频流处理
- **Canvas API** - 图像处理和数据提取
- **JavaScript** - 信号处理算法实现
- **HTML5/CSS3** - 响应式用户界面

## 📋 系统要求

### 浏览器支持

| 浏览器 | 版本要求 | 支持情况 |
|--------|---------|----------|
| Chrome | 60+ | ✅ 完全支持 |
| Firefox | 60+ | ✅ 完全支持 |
| Safari | 11+ | ✅ 完全支持 |
| Edge | 79+ | ✅ 完全支持 |
| Opera | 47+ | ✅ 完全支持 |

### 环境要求

- **HTTPS协议**：由于WebRTC安全策略，生产环境必须使用HTTPS
- **摄像头权限**：需要用户授权摄像头访问权限
- **充足光线**：建议在光线良好的环境下使用

## 📖 使用指南

### 最佳实践

1. **环境准备**
   - 确保充足的环境光线
   - 避免强光直射或背光
   - 使用稳定的支架固定设备

2. **测量姿势**
   - 正面面对摄像头
   - 将前额完全置于检测框内
   - 保持头部静止，避免说话

3. **提高准确性**
   - 测量前静坐2-3分钟
   - 避免剧烈运动后立即测量
   - 多次测量取平均值

### 常见问题

**Q: 为什么打不开摄像头？**
- 检查是否使用HTTPS访问
- 确认已授予摄像头权限
- 关闭其他占用摄像头的应用

**Q: 检测结果不准确怎么办？**
- 改善光线条件
- 确保面部在检测框内
- 保持绝对静止

**Q: 手机上无法使用？**
- 不要在微信/QQ内打开，使用浏览器
- iOS设备请使用Safari
- Android设备请使用Chrome

## ⚠️ 免责声明

**重要提示**：
- 本应用仅供演示和参考使用
- **不能替代专业医疗设备**
- 检测结果不具有医疗诊断价值
- 如需准确的心率数据，请使用医疗级设备
- 有心脏相关疾病请咨询医生

## 🤝 贡献指南

欢迎提交 Issue 和 Pull Request！

1. Fork 本仓库
2. 创建你的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交你的更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启一个 Pull Request

## 📝 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

## 🙏 致谢

- 感谢所有PPG相关研究论文的作者
- 感谢WebRTC社区的技术支持
- 特别感谢参与测试的朋友们

## 📧 联系方式

- 项目主页：[https://github.com/your-username/heart-rate-detector](https://github.com/your-username/heart-rate-detector)
- Issue反馈：[https://github.com/your-username/heart-rate-detector/issues](https://github.com/your-username/heart-rate-detector/issues)

---

<p align="center">
  Made with ❤️ by AI护工团队
</p>
