# 图片风格迁移学习项目
该项目基于paper [A Neural Algorithm of Artistic Style](https://arxiv.org/abs/1508.06576)以及paper [Semantic Style Transfer and Turning Two-Bit Doodles into Fine Artworks](https://arxiv.org/abs/1603.01768)。<br>
>* 第一篇paper，能够将一张内容图片和一张风格图片混搭到一起，产生出非常有艺术感的图片；<br>
>>* 效果![style_transfer_git.png](https://github.com/yhcc/style_transfer/blob/master/images/style_transfer_git.png)
>* 第二篇paper，image analogy: 通过对原图使用一张scratch图片进行标注，然后再利用另一张scratch图片即可生成与原图风格类似但内容完全不同的图片。<br>
>>* 效果![paper2_1_git](https://github.com/yhcc/style_transfer/blob/master/images/paper2_1_git.png)
>* 第二篇paper，style transfer: 通过同时使用四张图片，最终可以生成的结果为风格迁移、内容不变。<br>
>>* 效果![paper2_2_git](https://github.com/yhcc/style_transfer/blob/master/images/paper2_2_git.png)  

第一篇文章对应的代码在project.ipynb中  
内容图片在cell 5中加载，风格图片在cell 7中加载，修改对应路径即可使用不同的内容、风格图片。cell 73中alpha是多大程度上还原内容，beta是多大程度上还原风格。

第二篇文章对应的代码在extra.ipynb中  
图片加载在cell 96中。如果是image analogy，content image则使用一张noise照片即可，另外将cell 185中的beta设置为0。

# 说明  
该项目是使用Theano写成的，当前Theano相对cuda、cudnn比较滞后，可能出现无法正常运行的情况。正在重写一个pytorch版本的。现有的实现在效率上比较差，之后的pytorch版本应该会有改善。

# 下载vgg19.h5
https://gist.github.com/baraldilorenzo/8d096f48a1be4a2d660d
