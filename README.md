本項目為在naoGPT裏使用PyTorch對訓練數據進行收集並使用TensorBoard對手機後的數據進行可視化。  //
本次使用的源代碼來源于GitHub上開源的nanoGPT代碼，其地址為：https://github.com/karpathy/nanoGPT.git![image](https://github.com/user-attachments/assets/087642af-2b66-4797-875f-2e34da9cfa04) //
#操作步驟：
首先，服務器裏確認工具版本，本人使用的TensorBoard工具版本為：2.15.2；其餘工具版本推薦為：Python：3.9+；Pytouch：pytorch_v2.2.1+ ；
然後，修改GitHub上開源的nanoGPT代碼裏的train.py文件，將本代碼裏的train.py裏的代碼内容代替原内容；
隨後，在終端輸入`python train.py config/train_shakespeare_char.py     --wandb_log=False     --wandb_project=shakespeare-char     --batch_size=2     --block_size=32` 啓動訓練；
接著，在訓練完成後在終端輸入`tensorboard --logdir=./logs-5` ，再在瀏覽器打開本地地址http://localhost:6006 ，即可完成所有操作。

