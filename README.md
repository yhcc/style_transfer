# 图片风格迁移学习项目
该项目基于paper [A Neural Algorithm of Artistic Style](https://arxiv.org/abs/1508.06576)以及paper [Semantic Style Transfer and Turning Two-Bit Doodles into Fine Artworks](https://arxiv.org/abs/1603.01768)。<br>
>* 第一篇paper，能够将一张内容图片和一张风格图片混搭到一起，产生出非常有艺术感的图片；<br>
>>* 原图![原图](https://github.com/yhcc/style_transfer/blob/master/images/content_image.jpg)
>>* 星空版，风格图片在左下角![星空版](https://github.com/yhcc/style_transfer/blob/master/images/result1.png)
>>* 尖叫版，风格图片在左下角![尖叫版](https://github.com/yhcc/style_transfer/blob/master/images/result2.png)
>* 第二篇paper，通过对原图使用一张scratch图片进行标注，然后再利用另一张scratch图片即可生成与原图风格类似但内容完全不同的图片。<br>
>>* 原图<br>![Renoir](https://github.com/yhcc/style_transfer/blob/master/images/Renoir.jpg)
>>* 原图scratch图片，与原图对应<br>![scratch1](https://github.com/yhcc/style_transfer/blob/master/images/Renoir_sem.png)
>>* 目标scratch图片, 用户自己提供的<br>![scratch2](https://github.com/yhcc/style_transfer/blob/master/images/Landscape_sem.png)
>>* 生成图片<br>![生成图片](https://github.com/yhcc/style_transfer/blob/master/images/paper2_1.png)

图片Renoir.jpg+Renoir_sem.jpg+Landscape_sem.png生成了paper2_1.png

另外(这是另一种迁移学习，只需要提供一个sketch就可以把原有风格迁移学习出来)：

    Gogh.jpg+Gogh_sem.png + Seth_sem.png生成了paper2_2.png
    
    Seth.jpg+Seth_sem.png + Gogh_sem.png生成了paper2_3.png



project.ipynb based on A neural Algorithm of Artistic Style
	This scripts needs vgg_weights.h5 file to build vgg network.
	Unlike consistent parameter to get the best result, our script needs manual work during the training. After training some epoches, we need to change parameter slightly based on the result picture right now, and run accordingly.
#input
	Input style image is style_image.jpg(Result is result1.png) or style_image2.jpg(Result is result2.png), content image is always content_image.


extrac.ipynb based on Semantic style transfer and turning two-bit doodles into fine artwork
	This scripts needs vgg_weights.h5 file to build vgg network.
	Unlike consistent parameter to get the best result, our script needs manual work during the training. After training some epoches, we need to change parameter slightly based on the result picture right now, and run accordingly. However, semantic weight and weights between conv3_1 and conv4_1 highly affect the result.
#Input1
	Input style image: Renoir.jpg, style semantic image:Renoir_sem.png; Input content image:N/A, content semantic image:Lanscape_sem.png. Result is paper2_1.png
#Input2:
	Input style image: Gogh.jpg, style semantic image:Gogh_sem.png; Input content image:Seth.jpg, content semantic image:Seth_sem.png. And exchange style and content. Results are paper2_2.png,paper2_3.png.

If you want to run these codes, you can run cells one by one for both.

#download vgg19.h5
https://gist.github.com/baraldilorenzo/8d096f48a1be4a2d660d
