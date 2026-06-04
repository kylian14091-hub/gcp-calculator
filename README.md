# GCP 价格计算器

一个纯前端、单文件的 **Google Cloud 费用估算器**，零依赖、可离线使用。

🔗 **在线访问**：https://kylian14091-hub.github.io/gcp-calculator/

---

## ✨ 功能

- **16 类产品估算**：Compute Engine、GKE、Cloud Run、Cloud Functions、Cloud Storage、Filestore、Cloud SQL、Cloud Spanner、BigQuery、Pub/Sub、Cloud CDN、Cloud Load Balancing、Cloud NAT、Memorystore (Redis)、Cloud Logging、Cloud Monitoring。
- **完整机型库**：Compute Engine 覆盖 ~290 个机型（通用 E2/N1/N2/N2D/N4/T2D/T2A、计算优化 C2/C2D/C3/C3D/C4/C4A/H3、内存优化 M1/M2/M3、存储优化 Z3、加速器 G2/A2/A3），按系列分组选择。
- **🔍 智能匹配规格**：输入目标 vCPU / 内存，自动匹配「满足需求且最经济」的机型，一键填入配置。已接入 **Compute Engine、GKE 节点、Cloud SQL 实例**。
- **多区域定价**：覆盖 GCP 全部 ~41 个区域，按区域价格系数自动换算。
- **多种计费模式**：Compute Engine 支持按需 / CUD 1 年(-37%) / CUD 3 年(-55%) / Spot。
- **多产品叠加**：同时配置多个产品，汇总月费 / 年费，支持费用明细展开。
- **货币切换**：USD / CNY 即时切换。
- **导出**：CSV 导出、JSON 复制。
- **免费层提示**：自动扣除各产品免费配额。

## 🖥️ 使用方式

- 直接访问上方在线地址；或
- 下载 `index.html`（或 `gcp-calculator.html`），用浏览器双击打开即可（无需服务器）。

## 💱 价格数据来源与免责声明

- 价格主要参照 **Google Cloud 官方定价**（基准区域 **us-central1（爱荷华）/ 美国区，按需价**），并已对照官网逐产品核对、修正。
- 数据来源：
  - Compute / 磁盘 / GPU：https://cloud.google.com/compute/all-pricing
  - Cloud Storage：https://cloud.google.com/storage/pricing
  - BigQuery：https://cloud.google.com/bigquery/pricing
  - Cloud SQL：https://cloud.google.com/sql/pricing
  - Spanner：https://cloud.google.com/spanner/pricing
  - Memorystore：https://cloud.google.com/memorystore/docs/redis/pricing
  - Cloud Run / Functions / GKE / CDN / 网络 / 运维 / Filestore：对应官方 pricing 页面
- **区域系数为近似比例**（非逐 SKU 实价）；部分产品（如 RHEL/SLES 许可、pd-extreme 的预配 IOPS、BigQuery Editions 承诺折扣等）采用了简化建模。
- 本工具仅供**快速估算与对比参考**，不构成账单承诺。实际费用请以 [Google Cloud 官方定价计算器](https://cloud.google.com/products/calculator) 和你的真实账单为准。
- 价格会随官方调整而变化，请留意核对日期。

## 🔄 更新部署

修改后推送即可自动更新线上站点（约 1 分钟生效）：

```bash
git add -A
git commit -m "update"
git push
```

## 📄 许可

个人/内部估算用途，自由使用。
