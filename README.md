# 使用教程:

本項目為在nanoGPT裏使用PyTorch對訓練數據進行收集，並使用TensorBoard對收集後的數據進行可視化。   

本次使用的源代碼來源于GitHub上開源的nanoGPT代碼，其地址為：https://github.com/karpathy/nanoGPT.git
## 操作過程:

**首先**，服務器裏確認工具版本，本人使用的TensorBoard工具版本為：2.15.2；其餘工具版本推薦為：Python：3.9+；Pytorch：pytorch_v2.2.1+ ；

**然後**，需要修改GitHub上開源的nanoGPT代碼裏的train.py文件，即將本代碼裏的train.py裏的代碼内容代替原内容；

**隨後**，在終端輸入：
```bash
python train.py config/train_shakespeare_char.py     --wandb_log=False     --wandb_project=shakespeare-char     --batch_size=2     --block_size=32
```
即可啓動訓練；

**接著**，在訓練完成後在終端輸入`tensorboard --logdir=./logs-5` ，再在瀏覽器打開本地地址http://localhost:6006 ，即可完成所有操作。

