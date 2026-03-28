# 🌍 Global True Solar Time Calculator | 全球真太阳时精准计算器

A lightweight, purely frontend web application to calculate True Solar Time (TST) with astronomical precision, featuring smart DST (Daylight Saving Time) handling and global geolocation support. 

一款轻量级、纯前端的 Web 应用程序。利用天文级精度算法计算真太阳时，内置全球地理位置检索与智能夏令时防错机制。

---

## ✨ Features / 核心特性

- **Astronomical Precision (天文级精度)**: Uses the rigorous Spencer (1971) Fourier series formula to calculate the Equation of Time (EoT), ensuring high-accuracy TST results. / 采用天文学界权威的 Spencer (1971) 傅里叶级数公式计算均时差，确保极高的换算精度。
- **Smart DST Handling (智能夏令时防错)**: Automatically detects and offsets historical DST for any given location. Includes a manual override toggle to prevent "duplicate deductions" common in astrology/bazi tools. / 自动识别并扣除全球历史夏令时。独创“防重复扣除”开关，完美解决排盘工具界常见的夏令时重复计算痛点。
- **Global Geolocation (全球地理检索)**: Integrated with the Open-Meteo API. Simply input a city name or ZIP code to instantly retrieve precise longitude and timezone data without a massive local database. / 接入 Open-Meteo 接口，输入城市名、拼音或邮编即可瞬间获取精准经纬度与时区，彻底告别臃肿的本地数据库。
- **Zero Backend (零后端纯前端)**: Runs entirely in the browser. Ultra-fast, zero latency, and easily hostable on GitHub Pages. / 100% 纯前端运行，极速响应，保护隐私。
- **1-Click Share (一键复制分享)**: Formats complex calculation results into a clean, readable text block for easy sharing on mobile devices. / 针对移动端优化，一键将复杂的排盘数据格式化为美观的文本并存入剪贴板。

## 🚀 Demo / 在线体验
[Click here to use the calculator](https://[你的GitHub用户名].github.io/[你的仓库名]/) 
*(Note: Please replace the link with your actual GitHub Pages URL / 请将此链接替换为你真实的网页链接)*

## 🛠️ Tech Stack / 技术栈
- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Time/Timezone Engine**: [Luxon](https://moment.github.io/luxon/) (Handling IANA timezone database and historical DST)
- **Geolocation API**: [Open-Meteo Geocoding API](https://open-meteo.com/en/docs/geocoding-api) (Free & No API Key required)

## 📦 How to Use (Local Run) / 本地运行指南
1. Clone this repository or download the `index.html` file. / 克隆此仓库或直接下载 `index.html` 文件。
2. Double-click `index.html` to open it in any modern browser. / 双击文件在任何现代浏览器中打开即可使用。
3. No server or build tools required! / 无需配置服务器或打包工具！

## 📄 License / 开源协议
MIT License
