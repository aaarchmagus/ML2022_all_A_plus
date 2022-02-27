# Hw2 Classification 思路
- 因為聲音訊號資料點太多，通常會用 Conv1d 做 downsampling，模型部分參考 Hubert 的 FeatureEncoder（約 5 層 Conv1d，LayerNorm 跟 GELU，一切都寫在 transformers 的 Hubert 的原始碼裡了）
- 用 Conv1d 就不用管 concat_nframes 了
- 若覺得自己模型太強可使用 dropout 防止 overfitting
- AdamW betas 用 (0.9, 0.98)
- lr 1e-3，train 約 100 ~ 200 epochs, batch size 512 上下，可自行調整（很閒的話也可以用 batch size 4）
- 我本人的專業是做 Spoken Language Understanding, 常常拜讀（跪著）宏毅老師的論文（SUPERB 真的很厲害），覺得老師這次作業出得相當好，雖然知識量有點多，希望大家能努力搞懂 > <。另外推個陳縕儂老師的 miuLab，老師人真的很好，歡迎各位來當我的學弟妹呦～～
