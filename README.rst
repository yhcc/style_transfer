Initial repo for project

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
