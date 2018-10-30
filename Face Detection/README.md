# Face Detection

## 目录
### :cow: 主流方法

- [FaceBoxes](https://arxiv.org/pdf/1708.05234.pdf)
- [MTCNN](https://arxiv.org/pdf/1604.02878)



### :baseball: 数据集
- FDDB: [主页链接](http://vis-www.cs.umass.edu/fddb/) [论文链接](http://vis-www.cs.umass.edu/fddb/fddb.pdf)
- PASCAL face dataset: [主页链接](http://host.robots.ox.ac.uk/pascal/VOC/databases.html)
- [WIDER FACE](#WIDER-FACE): [主页链接](http://mmlab.ie.cuhk.edu.hk/projects/WIDERFace/) [论文链接](https://arxiv.org/pdf/1511.06523.pdf)
- AFW dataset: [主页链接](https://www.ics.uci.edu/~xzhu/face/)（不可访问）


### :notebook: 论文
- S<sup>3</sup>FD: Single Shot Scale-invariant Face Detector, S.Zhang et al. (ICCV 2017) [[pdf]](https://arxiv.org/pdf/1708.05237.pdf)
- SSH: Single Stage Headless Face Detector, M.Najibi et al. (ICCV 2017) [[pdf]](https://arxiv.org/pdf/1708.03979.pdf)
- SFace: An Efficient Network for Face Detection in Large Scale Variations, J.Wang et al. (CVPR 2018) [[pdf]](https://arxiv.org/pdf/1804.06559.pdf)
- Face R-CNN, H.Wang et al. [[pdf]](https://arxiv.org/pdf/1706.01061.pdf)
- Face R-FCN, H.Wang et al. [[pdf]](https://arxiv.org/pdf/1709.05256.pdf)


### :rocket: 项目
- **libfacedetection** [[GitHub仓库链接]](https://github.com/ShiqiYu/libfacedetection)
- **face-api.js**  [[GitHub仓库链接]](https://github.com/justadudewhohacks/face-api.js) [[Demo]](https://justadudewhohacks.github.io/face-api.js/face_and_landmark_detection) [[入门文章]](https://itnext.io/face-api-js-javascript-api-for-face-recognition-in-the-browser-with-tensorflow-js-bcc2a6c4cf07)



## 详细介绍

### :cow: 主流方法

### :baseball: 数据集
#### WIDER FACE
> WIDER FACE dataset is a face detection benchmark dataset, of which images are selected from the publicly available WIDER dataset. We choose 32,203 images and label 393,703 faces with a high degree of variability in scale, pose and occlusion as depicted in the sample images. WIDER FACE dataset is organized based on 61 event classes. For each event class, we randomly select 40%/10%/50% data as training, validation and testing sets. We adopt the same evaluation metric employed in the PASCAL VOC dataset. Similar to MALF and Caltech datasets, we do not release bounding box ground truth for the test images. Users are required to submit final prediction files, which we shall proceed to evaluate.

几项关键指标：`393703`人脸，`32203`图片，`40%/10%/50%`划分训练、验证、测试集，`61`项事件分类。

评价标准通常可划分为：`Scenario-Ext` 和 `Scenario-Int`，前者表示用任意外部数据进行训练，后者表示用 `WIDER FACE` 的 `training/validation set` 进行训练，两者都在 `WIDER FACE` 的 `testing set` 进行测试。
目前主流方法通常采用 `Scenario-Int` 评价标准。

更多详情可以参考 [WIDER FACE: A Face Detection Benchmark](http://mmlab.ie.cuhk.edu.hk/projects/WIDERFace/)


