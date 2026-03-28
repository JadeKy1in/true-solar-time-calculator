📝 开发日志 / Development Log
项目名称 / Project Name: 全球真太阳时精准计算器 / Global True Solar Time Calculator
核心技术 / Tech Stack: HTML5, CSS3, Vanilla JavaScript, Luxon (Timezone Handling), Open-Meteo API

🚀 v1.0：架构确立与核心算法验证 / Concept & Core Logic
[CN] 确立项目核心架构，采用纯前端单文件（HTML/JS）方案，确保跨平台（PC/移动端）兼容性以及支持本地离线运行。

[EN] Established the core architecture using a pure frontend, single-file (HTML/JS) approach to ensure cross-platform compatibility and local offline execution.

[CN] 初步测试了基于本地 CSV 数据库（美国邮编与世界时区）的数据读取，实现了基于 Luxon 库的 UTC 转换与基础均时差（EoT）换算逻辑。

[EN] Initially tested data retrieval using local CSV databases (US ZIP & World Timezones). Implemented UTC conversion and basic Equation of Time (EoT) calculation using the Luxon library.

⚡️ v2.0：API 迁移与天文级精度升级 / API Migration & Astronomical Upgrade
[CN] 性能重构：发现 160MB 乃至更庞大的本地地名数据库会导致严重的浏览器性能瓶颈。果断弃用 CSV 方案，全面接入 Open-Meteo 免费地理 API，实现零体积、高精度的全球经纬度与时区实时检索。

[EN] Performance Refactoring: Identified severe browser performance bottlenecks caused by massive (160MB+) local geolocation CSV databases. Deprecated the CSV approach and integrated the free Open-Meteo Geocoding API, enabling zero-footprint, high-precision retrieval of global coordinates and timezones.

[CN] 算法升级：将核心算法从简易三角函数升级为天文学界权威的 Spencer (1971) 傅里叶级数公式，大幅提升真太阳时的计算精度，并将夏令时处理逻辑下沉至 UTC 转换层，从根本上规避时间换算错误。

[EN] Algorithm Upgrade: Upgraded the core algorithm from simple trigonometric functions to the authoritative Spencer (1971) Fourier series formula for maximum astronomical accuracy. Moved DST handling logic down to the UTC conversion layer to fundamentally prevent time conversion errors.

🌐 v3.0：国际化与用户体验优化 / Internationalization & UX Optimization
[CN] 全面推行中英双语界面，优化 UI 视觉层次，提升国际化可用性。

[EN] Rolled out a comprehensive bilingual (Chinese/English) user interface and optimized visual hierarchy to enhance international usability.

[CN] 新增功能：为优化移动端社交分享体验，新增“一键复制”功能，可将复杂的排盘计算结果自动格式化为美观的排版文本并一键存入剪贴板。

[EN] New Feature: To optimize the mobile social sharing experience, added a "1-Click Copy" feature that automatically formats complex calculation results into a clean text layout and saves it to the clipboard.

🛡️ v4.1 (Current)：边缘测试与防呆机制 / Edge Cases & Foolproof Mechanisms
[CN] 痛点解决 (夏令时防重复扣除)：新增手动/自动双模开关。针对专业用户可能已提前扣除夏令时的情况，提供底层算法豁免权，完美解决排盘工具界常见的“系统与用户重复扣除夏令时”的行业痛点。

[EN] Pain Point Resolved (DST Duplicate Deduction): Introduced an Auto/Manual toggle. Granted algorithmic exemption for professional users who might have already deducted the DST offset, perfectly solving the common industry issue of "duplicate DST deduction by both user and system."

[CN] 智能错误拦截：针对底层数据库对中国大陆 6 位邮编支持匮乏的客观限制，编写了正则表达式拦截器。当用户输入 6 位数字且查询失败时，精准引导用户改用城市或区县拼音查询，降低用户挫败感。

[EN] Smart Error Interception: Implemented a Regex interceptor to address the underlying database's limited support for 6-digit Chinese ZIP codes. When a 6-digit input fails, it precisely guides the user to search by city or district name, reducing user frustration.

[CN] 完善了全量双语报错弹窗与夏令时触发警告。

[EN] Perfected fully bilingual error pop-ups and active DST warning alerts.
