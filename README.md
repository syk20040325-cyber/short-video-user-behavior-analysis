# Short Video User Behavior Analysis

## 业务背景
基于 1.9 万条真实短视频（TikTok/Douyin）播放与互动数据，诊断内容表现与用户互动特征。核心指标包括：视频播放量、点赞/评论/分享/下载量、互动转化率。

## 分析目标
1. 清洗原始视频数据，衍生“总互动数”、“互动转化率”与“时长分桶”指标。
2. 使用 SQL 计算大盘核心指标，并搭建「播放量 → 点赞量 → 深度互动量」转化漏斗，定位流失节点。
3. 按内容性质（Claim/Opinion）、认证状态（Verified/Not Verified）与视频时长进行多维度下钻分析。
4. 通过数据可视化对比不同群体行为差异，输出内容分发与创作者运营方向的业务建议。

## 技术栈
SQL, Python (Pandas, Matplotlib, Seaborn, Sqlite3)

## 项目结构
- `data/`: 原始脱敏数据集 (tiktok_dataset.csv)
- `notebook/`: 包含数据清洗、SQL 聚合、可视化代码 (behavior_analysis.ipynb)
- `report/`: 包含详细分析报告 (analysis_report.md) 与高清可视化图表 (figures/)

## 核心洞察
- **大盘互动率极强**：整体互动转化率达到 33.5%，说明争议/观点类内容极易引发参与。
- **时长反常识**：31-60 秒视频的互动率（33.67%）高于 15 秒以内短视频（33.18%）。
- **内容为王**：带有事实声明（claim）的视频互动率是纯个人观点（opinion）的 1.5 倍，且认证大V与普通号的互动率无明显差异。
