# 更新日志

## 2026-10-08
### 新增
- **辟邪 RVC 模型（exp_bixie3）**：RVC 训练（32k/v2/40轮/预训练权重/7切片），含模型 + added_IVF31 索引，支持翻唱与变声。`辟邪模型.zip`
- **四不相 GPT-SoVITS（e15）**：干净人声重训的文字转语音模型，含 GPT 权重 `sibuxiang-e15.ckpt` 与 SoVITS 权重 `sibuxiang_e15_s900_l32.pth`。`四不相GPTSoVITS.zip`

### 仓库现有内容
| 模型 | 类型 | 说明 |
| --- | --- | --- |
| 天禄new3 | RVC 翻唱 | `天禄new3模型.zip` |
| 四不相v2 | RVC 翻唱 | `四不相v2模型.zip` |
| 辟邪 exp_bixie3 | RVC 翻唱/变声 | `辟邪模型.zip`（本次新增） |
| 四不相 | GPT-SoVITS TTS | `四不相GPTSoVITS.zip`（本次新增） |

### 备注
- 辟邪/四不相翻唱建议参考 README 中的参数（index_rate、protect、pitch）。
- RVC 推理输出为 int16 量纲，混音前需归一化，详见 README。
