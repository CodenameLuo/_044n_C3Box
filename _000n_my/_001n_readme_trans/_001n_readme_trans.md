<p align="center">
<img src="../../resources/logo.png"  width="800px">
</p>

<p align="center">
  <a href="#introduction">🎉简介</a> •
  <a href="#methods-reproduced">🌟已复现方法</a> •
  <a href="#whats-new">📰最新动态</a> •
  <a href="#how-to-use">☄️使用方法</a> •
  <a href="#acknowledgments">👨‍🏫致谢</a> •
  <a href="#contact">🤗联系方式</a>
</p>

---

<a id="introduction"></a>

## 🎉 简介

欢迎使用 C3Box，这是一个基于 CLIP 的持续学习工具箱 <a href="https://arxiv.org/abs/2601.20852">[论文]</a>。一方面，C3Box 实现了一些先进的、基于 CLIP 的类增量学习算法，例如 CLG-CBM、PROOF 和 ENGINE。另一方面，C3Box 也适配了典型的类增量学习算法（*例如* FOSTER 和 MEMO）以及基于 ViT 的类增量学习算法（*例如* L2P 和 DualPrompt），用于评估它们的有效性。

**如果你在自己的工作中使用了本仓库的任何内容，请引用以下 BibTeX 条目：**

    @article{sun2026c3box,
        title={C3Box: A CLIP-based Class-Incremental Learning Toolbox},
        author={Sun, Hao and Zhou, Da-Wei},
        journal={arXiv preprint arXiv:2601.20852},
        year={2026}
    }
    
    @inproceedings{zhou2024continual,
        title={Continual learning with pre-trained models: A survey},
        author={Zhou, Da-Wei and Sun, Hai-Long and Ning, Jingyi and Ye, Han-Jia and Zhan, De-Chuan},
        booktitle={IJCAI},
        pages={8363-8371},
        year={2024}
    }

    @article{zhou2024class,
        author = {Zhou, Da-Wei and Wang, Qi-Wei and Qi, Zhi-Hong and Ye, Han-Jia and Zhan, De-Chuan and Liu, Ziwei},
        title = {Class-Incremental Learning: A Survey},
        journal={IEEE Transactions on Pattern Analysis and Machine Intelligence},
        volume={46},
        number={12},
        pages={9851--9873},
        year = {2024}
    }

<a id="whats-new"></a>

## 📰 最新动态

- [2026-01]🌟 C3Box 初始版本发布 <a href="https://arxiv.org/abs/2601.20852">[论文]</a>。
- [2026-01]🌟 发布代码。

<a id="methods-reproduced"></a>

## 🌟 已复现方法

- `FineTune`：基线方法，直接在新任务上更新参数。
- `ZS-CLIP`：基线方法，用作预训练 CLIP 在下游任务上的性能参照。
- `FOSTER`：用于类增量学习的特征增强与压缩。ECCV 2022 [[论文](https://arxiv.org/abs/2204.04662)]
- `MEMO`：一个模型还是 603 个样本：面向内存高效类增量学习。ICLR 2023 Spotlight [[论文](https://openreview.net/forum?id=S07feAlQHgM)]
- `L2P`：面向持续学习的 Prompt 学习。CVPR 2022 [[论文](https://arxiv.org/abs/2112.08654)]
- `DualPrompt`：DualPrompt：面向无回放持续学习的互补 Prompt。ECCV 2022 [[论文](https://arxiv.org/abs/2204.04799)]
- `CODA-Prompt`：CODA-Prompt：面向无回放持续学习的持续分解式注意力 Prompt。CVPR 2023 [[论文](https://arxiv.org/abs/2211.13218)]
- `Ease`：面向基于预训练模型的类增量学习的可扩展子空间集成。CVPR 2024 [[论文](https://arxiv.org/abs/2403.12030)]
- `SimpleCIL`：重新审视基于预训练模型的类增量学习：只需要泛化性与适应性。IJCV 2024 [[论文](https://arxiv.org/abs/2303.07338)]
- `APER`：重新审视基于预训练模型的类增量学习：只需要泛化性与适应性。IJCV 2024 [[论文](https://arxiv.org/abs/2303.07338)]
- `TUNA`：面向基于预训练模型的类增量学习，整合任务特定适配器与通用适配器。ICCV 2025 [[论文](https://arxiv.org/abs/2508.08165)]
- `RAPF`：使用 CLIP 进行类增量学习：自适应表征调整与参数融合。ECCV 2024 [[论文](https://arxiv.org/abs/2407.14143)]
- `MG-CLIP`：Mind the Gap：在基于 CLIP 的持续学习中保持并补偿模态间隙。ICCV 2025 [[论文](https://arxiv.org/abs/2507.09118)]
- `CLG-CBM`：面向可解释持续学习的语言引导概念瓶颈模型。CVPR 2025 [[论文](https://arxiv.org/abs/2503.23283)]
- `PROOF`：面向视觉-语言模型的无遗忘学习。TPAMI 2025 [[论文](https://arxiv.org/abs/2305.19270)]
- `ENGINE`：面向基于 CLIP 的类增量学习的外部知识注入。ICCV 2025 [[论文](https://arxiv.org/abs/2503.08510)]
- `BOFA`：BOFA：面向基于 CLIP 的类增量学习的桥接层正交低秩融合。AAAI 2026 [[论文](https://arxiv.org/abs/2511.11421)]

<a id="how-to-use"></a>

## ☄️ 使用方法

### 🕹️ 克隆

克隆这个 GitHub 仓库：

```bash
git clone https://github.com/LAMDA-CL/C3Box
cd LAMDA-C3Box
```

### 🗂️ 依赖

1. [torch 2.0.1](https://github.com/pytorch/pytorch)
2. [torchvision 0.15.2](https://github.com/pytorch/vision)
3. [timm 0.6.12](https://github.com/huggingface/pytorch-image-models)
4. [tqdm](https://github.com/tqdm/tqdm)
5. [numpy](https://github.com/numpy/numpy)
6. [scipy](https://github.com/scipy/scipy)
7. [easydict](https://github.com/makinacorpus/easydict)
8. [open-clip 2.17.1](https://github.com/mlfoundations/open_clip/releases/tag/v2.17.1)

### 🔑 运行实验

1. 编辑 `[MODEL NAME].json` 文件，用于设置全局配置和超参数。
2. 运行：

    ```bash
    python main.py --config=./exps/[MODEL NAME].json
    ```

3. `hyper-parameters`

    使用 C3Box 时，可以在对应的 json 文件中编辑全局参数和算法特定超参数。

    这些参数包括：

   - **model_name**：模型名称应从上面列出的 11 种方法中选择，*即* `finetune`、`zs_clip`、`foster`、`memo`、`simplecil`、`l2p`、`dual`、`coda`、`ease`、`aper`、`tuna`、`rapf`、`clg_cbm`、`mg_clip`、`proof`、`engine` 和 `bofa`。
   - **init_cls**：初始增量阶段中的类别数量。由于 CIL 配置包含不同的设置，并且初始阶段的类别数可能不同，本框架支持以多种方式定义初始阶段。
   - **increment**：第 $i$ 个增量阶段中的类别数量，其中 $i$ > 1。默认情况下，所有增量阶段的类别数量相同。
   - **backbone_type**：增量模型的骨干网络。它可以从 Timm 库提供的多种预训练模型中选择，例如用于 **ViT-B/16** CLIP 的 **LAION-400M** 和 **OpenAI**。
   - **seed**：随机种子，用于打乱类别顺序。默认设置为 1993，遵循 iCaRL 的 benchmark 设置。
   - **fixed_memory**：布尔参数。设置为 true 时，模型会为每个类别维护固定数量的记忆样本。设置为 false 时，模型会为每个类别保留动态分配的记忆样本。
   - **memory_size**：增量学习过程中的样本总数。如果 `fixed_memory` 设置为 false，假设当前阶段共有 $K$ 个类别，则模型会为每个类别保留 $\left[\frac{{memory-size}}{K}\right]$ 个样本。**ZS-CLIP、SimpleCIL、ADAM、EASE、TUNA、CLG_CBM、MG_CLIP、ENGINE 和 BOFA 不需要样本。** 因此，与样本相关的参数不会被使用。
   - **memory_per_class**：如果 `fixed memory` 设置为 true，模型会为每个类别保留固定数量的 `memory_per_class` 个样本。

### 🔎 数据集

我们已经实现了以下数据集的预处理：

- **CIFAR100**：会由代码自动下载。
- **CUB200**：Google Drive：[链接](https://drive.google.com/file/d/1XbUpnWpJPnItt5zQ6sHJnsjPncnNLvWb/view?usp=sharing) 或 OneDrive [链接](https://entuedu-my.sharepoint.com/:u:/g/personal/n2207876b_e_ntu_edu_sg/EVV4pT9VJ9pBrVs2x0lcwd0BlVQCtSrdbLVfhuajMry-lA?e=L6Wjsc)
- **ImageNet-R**：Google Drive：[链接](https://drive.google.com/file/d/1SG4TbiL8_DooekztyCVK8mPmfhMo8fkR/view?usp=sharing) 或 OneDrive：[链接](https://entuedu-my.sharepoint.com/:u:/g/personal/n2207876b_e_ntu_edu_sg/EU4jyLL29CtBsZkB6y-JSbgBzWF5YHhBAUz1Qw8qM2954A?e=hlWpNW)
- **ObjectNet**：OneDrive：[链接](https://entuedu-my.sharepoint.com/:u:/g/personal/n2207876b_e_ntu_edu_sg/EZFv9uaaO1hBj7Y40KoCvYkBnuUZHnHnjMda6obiDpiIWw?e=4n8Kpy)。如果文件太大无法下载，也可以参考 [filelist](https://drive.google.com/file/d/147Mta-HcENF6IhZ8dvPnZ93Romcie7T6/view?usp=sharing) 和处理 [代码](https://github.com/zhoudw-zdw/RevisitingCIL/issues/2#issuecomment-2280462493)。
- **Cars**：Google Drive：[链接](https://drive.google.com/file/d/1D8ReAuOPenWi6SMNUrOZhbm6ViyhDHbL/view?usp=sharing  ) 或 OneDrive：[链接](https://njuedu-my.sharepoint.cn/:u:/g/personal/ky2409911_365_nju_edu_cn/EbT1XAstg51Mpy82uHM0D2EBJLrtzmr_V64jeBRjqyyTnQ?e=h6g1rM)
- **UCF**：Google Drive：[链接](https://drive.google.com/file/d/1Ng4w310_VDqpKbc7eYaumXTOiDxI02Wc/view?usp=sharing) 或 OneDrive：[链接](https://njuedu-my.sharepoint.cn/:u:/g/personal/ky2409911_365_nju_edu_cn/EU2qHQXjASdLh1jIl6ihZmcB6G2KvqmSw-sTlZKDE6xPbg?e=7ezvTr)
- **Aircraft**：Google Drive：[链接](https://drive.google.com/file/d/1xI5r1fU0d6Nff51HuOo5w-e4sGEP46Z2/view?usp=drive_link) 或 OneDrive：[链接](https://njuedu-my.sharepoint.cn/:u:/g/personal/ky2409911_365_nju_edu_cn/ETVliZnmPY9AvZZgcFFJ6jMB2c7TRvcq7-gso2Aqvdl_VQ?e=pWXqdP)
- **Food**：Google Drive：[链接](https://drive.google.com/file/d/1rupzXpwrbxki4l-RVmsRawhz1Cm0lDY5/view?usp=drive_link) 或 OneDrive：[链接](https://njuedu-my.sharepoint.cn/:u:/g/personal/ky2409911_365_nju_edu_cn/Eb4xfptD4L5Egus-SiYxrIcBDH1VewLGp4kzyACGF_Na_w?e=duA3Ia)
- **SUN**：OneDrive：[链接](https://njuedu-my.sharepoint.cn/:u:/g/personal/ky2409911_365_nju_edu_cn/EcQq1-1pFulKstYtdknB4O8BGo0hnlDRarAwB4wFEgkx0Q?e=YZ0xYV)
- **TV100**：OneDrive：[链接](https://njuedu-my.sharepoint.cn/:u:/r/personal/ky2409911_365_nju_edu_cn/Documents/TV100/TV100.zip?csf=1&web=1&e=XNpitj)

> 这些子集采样自原始数据集。请注意，我没有分发这些数据集的权利。如果分发行为违反许可证，我将改为提供文件名。

当训练数据集**不是** `CIFAR100` 时，应在 `utils/data.py` 中指定数据集文件夹。

```python
    def download_data(self):
        assert 0,"You should specify the folder of your dataset"
        train_dir = '[DATA-PATH]/train/'
        test_dir = '[DATA-PATH]/val/'
```

<a id="acknowledgments"></a>

## 👨‍🏫 致谢

感谢以下仓库为我们的工作提供了有用的组件和函数。

- [PyCIL](https://github.com/G-U-N/PyCIL)
- [PILOT](https://github.com/LAMDA-CL/LAMDA-PILOT)

<a id="contact"></a>

## 🤗 联系方式

如果有任何问题，欢迎通过 issue 提出新功能建议，或联系作者：**Hao Sun**（[sunhao@lamda.nju.edu.cn](mailto:sunhl@lamda.nju.edu.cn)）和 **Da-Wei Zhou**（[zhoudw@lamda.nju.edu.cn](mailto:zhoudw@lamda.nju.edu.cn)）。祝你使用代码愉快。
