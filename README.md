# ChineseFaces_dataset
High quality deepfake dataset constructed using Chinese faces.
# 数据集名称：ChineseFaces

**制作单位**：西安电子科技大学

**实验室**：现代图像处理实验室

**实验室研究方向**：智能图像处理、智能视频分析、北斗卫星导航定位算法研究与应用

## 1. 数据集创立初衷：

由于当前所用的人脸数据集基本都来自国外，其包含的人脸大多为外国人脸，对于我国的研究者相当不便。因此，我们通过挑选合适视频、并使用人脸身份替换、人脸表情驱动和人脸属性驱动技术，精心构建了一个较大规模的中国人脸深度伪造数据集，供有需要的研究人员下载使用。

该数据集的贡献：

- 首次提供了全为中国人的人脸数据集；
- 首次提供了属性编辑的人脸视频数据集。

## 2. 数据集介绍

- 规模：
  - 真实视频数量：300个（女性：150个，男性：150个）

- 伪造类型（3种）：
  - 身份替换：300个
  - 表情驱动：300个
  - 属性编辑（年龄编辑）：300个

- 视频时长：15s

- 版本（4种）： 
  - c0  - 原始版本；
  - c23 - 高质量压缩版本（采用H.264压缩格式，压缩质量为23）；
  - c35 - 中等质量压缩版本（采用H.264压缩格式，压缩质量为35）；
  - c40 - 低质量压缩版本（采用H.264压缩格式，压缩质量为40）；

### 2.1 数据集目录概览：

```python
--ChineseFaces
  --c0
    --attribute_edit		# 属性编辑视频
    --avatar				# 表情驱动视频
    --raw					# 真实视频
    --swap					# 身份替换视频
  --c23
    -attribute_edit
    --avatar
    --raw
    --swap
  --c35
	--attribute_edit
    --avatar
    --raw
    --swap
  --c40
	--attribute_edit
    --avatar
    --raw
    --swap
```

### 2.2 真实视频（raw）

我们从哔哩哔哩平台的三位访谈类UP主——魔都欧叔【[魔都欧叔](https://space.bilibili.com/273077414?spm_id_from=333.337.0.0)】、二狗App-单身青年故事【[二狗App-单身青年故事](https://space.bilibili.com/524930260?spm_id_from=333.337.0.0)】和凉子访谈录【[凉子访谈录](https://space.bilibili.com/496688267?spm_id_from=333.337.0.0)】的个人空间一共收集了300个不同人物的访谈视频，包括150名男性和150名女性，这些视频的长度都在10分钟左右。由于源视频时长太长，我们仅仅在每个视频中截取了15s的片段作为我们的源人脸视频，按顺序编号从001~300依次命名，视频的分辨率为1280×720，帧速率为30帧/秒或25帧/秒。

### 2.3 人脸替换视频（swap）：

- 人脸替换的概念：人脸交换需要两张不同的人脸作为原料，分别称作源人脸和目标人脸，对于源人脸和目标人脸的定义，学术界一直没有统一的定论，在我们的数据集中，我们将源人脸定义为提供人脸身份的人脸，而将目标人脸定义为提供表情和背景的人脸，也就是说，我们将源人脸的身份替换给了目标人脸，交换后的人脸相较于目标人脸，只是人脸身份不同，其余信息均相同。

- 数量：300个

- 伪造方法：SwapFace【[Swapface](https://swapface.org/#/home)】

### 2.4 表情驱动视频（avatar）：

- 表情驱动的概念：给定一张要驱动的目标人脸头像，再给定一段源人脸人脸，为要驱动的目标人脸提供驱动动作。

- 数量：300个

- 伪造方法：ICCV2023-MCNET【[ICCV2023-MCNET](https://github.com/harlanhong/ICCV2023-MCNET)】

### 2.5 属性编辑视频（attribute_edit）：

- 属性编辑的概念：给定一张人脸图像，对这张给定人脸的发色、胡子、是否秃头、年龄、性别、妆容进行编辑。在我们的数据集中，我们对源人脸视频的年龄属性进行了编辑，编辑因子均为2.0。

- 数量：300个

- 伪造方法：StyleGANEX【 [StyleGANEX](https://github.com/williamyang1991/StyleGANEX?tab=readme-ov-file)】

## 数据集展示

![](E:\data_made\readme.jpg)

## 3. 下载链接

- 百度网盘链接：链接：https://pan.baidu.com/s/1K79SCHdH5qAeNAkCLvNwUA  提取码：y9vr 
- 谷歌云盘链接：
  - c40: https://drive.google.com/file/d/171T8mFWc1YjPS-gComjBtEPz_MlwaREI/view?usp=sharing
  - c35: https://drive.google.com/file/d/1xO2QR_YHtJ0f43n22vRYoqNHIYmYsJom/view?usp=sharing
  - c23: https://drive.google.com/file/d/1EQd9BMG_qtSqyB2fIjs_iuddy-Mi0Q6f/view?usp=sharing
  - c0: https://drive.google.com/file/d/1JF9oapy7mWEcPaQRIHxYr8SBcKf5xt2w/view?usp=sharing

