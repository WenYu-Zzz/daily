# Image Colorization

Student Name: 杨钊，顾隽逸

Student ID: SID11813227, SID11910424



### 1. Introduction

  The topic chosen by our group is Image Colorization, though the first color image was taken in 1860, it was not until around 1970 that it began to be popular in the world. For decades, many film creators have opposed the idea of coloring B&W films and images, they regarded it as a destruction of art, but today it is accepted as an enhancement of art form. 
 
  In the image coloring task, our goal is to generate a color image with a given gray input image. This problem is challenging because it is multimodal which a single gray image may correspond to many reasonable color images. Therefore, traditional models usually rely on important user input and input gray image content. Colorization of images is a challenging problem due to the varying conditions of imaging that need to be dealt via a single algorithm. 



### 2. Related Works
#### Main networks:
- Plain networks: the traditional convolutional network structure algorithm whose network structure does not contain a skip layer
- User-Guided networks: the networks that require color values to be entered by the user at a specific layer of the network.
- Domain-Specific Colorization networks: Color images in specific fields, such as near-infrared images, synthetic aperture radar, radar, and skeleton images.
- Text-based colorization networks: Color the image according to the input described in this article.
- Diverse colorization networks: instead of restoring the original color of the image, different colored images are generated.
- Multi-path networks: Learning networks with different characteristics in different network paths.
- Examplar-based colorization networks: A reference learning sample is given by the user during shading.

#### Main dataset:
- COCO-stuff dataset
- PASCAL VOC dataset
- CIFAR datasets
- ImageNet ILSVRC2012
- Palette-and-Text dataset





### 3. Method

There are some pre and post-processing steps: convert to Lab space, resize to 256x256, colorize, and concatenate to the original full resolution, and convert to RGB.
```python
import colorizers
colorizer_eccv16 = colorizers.eccv16().eval()
colorizer_siggraph17 = colorizers.siggraph17().eval()
```



### 4. Experiments

#### 4.1 Datasets

We used two pictures taken by ourselves in SUSTC and some pictures in the test set as the test, The photos we took are as follows.

##### Original images:

![28278D8B2C394F598BBC4177014D93FE](https://user-images.githubusercontent.com/85725490/212480492-b7d71721-7648-4fd6-ad03-b9a85c4b1ce5.png)
![D76D4A0DC9ECD8EBE1E69F7241C40DE2](https://user-images.githubusercontent.com/85725490/212480542-6f8cc2cb-b30a-4480-9679-805d3bd27b42.png)

##### Convert it to B&W images:

![278529F5B5C1B54DEC7CA2B1D472DB12](https://user-images.githubusercontent.com/85725490/212480730-46e29774-2e5f-4f05-be1c-4c6e21fdbaa7.png)
![2E075365FDA920E29493194019266434](https://user-images.githubusercontent.com/85725490/212480740-9823a0db-aa37-4e9a-985c-3a1d1e198798.png)






#### 4.2 Implementation Details

#### 4.3 Metrics

#### 4.4 Experimental design & results

##### some results:
![3342EFB49B59262C99C8621D856B926F](https://user-images.githubusercontent.com/85725490/212480818-002fdd33-4e89-4259-abdd-f2b205e64b5d.png)
![50B28F12C94D898EBE82F811877FF1B4](https://user-images.githubusercontent.com/85725490/212481313-4723f4a6-47ce-40bd-868d-868d6b270f85.png)





### 5. Conclusion

All of the pictures we took were sunset pictures, of which the color effect of ECCV is better than that of SIGGPATH, and the latter's restoration effect is more inclined to the pictures in the daytime. In the image coloring task, the environment and time factors in the image will have a great impact on the shading effect.Therefore, adding some text descriptions can make the effect of picture coloring more natural and full



#### Reference





### Contributions

- 杨钊 (SID11813227):50%

- 顾隽逸 (SID11910424):50%

