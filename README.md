# SibuxiangTianluRVCmodel
this is sibuxiang and tianlu's RVCmodel
用RVC模型训练出来的天禄和四不相的声音模型，因为训练素材较少，四不相的模型可能会有
轻微的咬字问题，如遇到该问题，请尝试调整翻唱参数，protect参数尽量保持在0.33左右，太高可能会把人声中的辅音滤掉，导致咬字不清
两款模型的需要index_rate大约在0.6左右，天禄模型如果觉得声音不像可以尝试调到1.0
两款模型f0都使用rmvpe采样
天禄模型建议pitch=-1（若是同性别）
天禄模型生成的音乐可能太过平滑，如遇到此问题，请自行进行后期处理，或找我拿成品文件
如果是女声转男声，则pitch=-12左右，如果是同性则不变（pitch=0）或者向上调1或2个半音（pitch=1或2）
详见MODEL_USAGE.md

---

## 辟邪模型（exp_bixie3，RVC翻唱/变声）
用RVC训练出的辟邪声音模型，`辟邪模型.zip` 内含：
- 模型：`exp_bixie3.pth`（32k / v2 / 40轮 / 预训练权重 / 7切片）
- 索引：`exp_bixie3_added_IVF31_Flat_nprobe_1_exp_bixie3_v2.index`
- 训练素材 `bixie.wav`（约64秒，已做伴奏分离）

翻唱参数参考：`f0=rmvpe`、`index_rate≈0.7`、`protect≈0.55`、`rms_mix_rate≈0.4`。女声转男声建议 `pitch≈-3` 或更低，具体按听感微调。注意RVC推理输出为int16量纲，混音前需归一化到与伴奏同量纲，否则伴奏会被盖没。

## 四不相 GPT-SoVITS（文字转语音）
用GPT-SoVITS v3在干净人声素材上训练的四不相TTS模型（e15），`四不相GPTSoVITS.zip` 内含：
- GPT模型：`sibuxiang-e15.ckpt`
- SoVITS模型：`sibuxiang_e15_s900_l32.pth`

用法：在GPT-SoVITS推理界面分别选择上述GPT与SoVITS权重，输入文本即可合成四不相语音。
