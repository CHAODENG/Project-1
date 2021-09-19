# Self-supervision for graph data structures
This topic covers the experiment with self-supervised models to find relationship between data to display and predict. We can extract some useful data through digging from the unsigned graphs through Self-supervision learning.

## Semi-supervision vs Self-supervision
In recent years, due to the ubiquity of graph data sturcture, graph-based deep learning has attracted more and more attention and researchers from the field of artificial intelligence. However, before self-supervision learning, most of the deep learning works on graphs using semi-supervised learning, in which the model is based on manually annotated information for downstream task training. Although semi-supervised graph learning has been successful, it still has some shortcomings due to its heavy reliance on these label information: **the high-cost of obtaining ground-truth label, poor generalization ability because of overfitting, weak robustness under adversarial attacks.**

To address issues, self-supervision is a promising and trending paradigm which extracts informative knowledge from well-design tasks without relying on annotated information. It improves the generalization ability and has better performance than semi-supervised learning.

### Why SELF-SUPERVISION？
Self-supervision optimizes tasks by training models so it further reduces the reliance on manual labels. Through training by self-supervised learning, it can help model learn from more generalized representations from unlabel data.Most of the work of graph learning overemphasizes the role of labels, while ignoring the rich underlying structure and contributive information. The design of various Self-supervised learning helps to solve this situation. In addition, the cost of collecting graph label information is high, which prevents most existing methods from being applied to real-world data. **Therefore, SSL(Self-supervised learning) reduces the reliance on artificial tags which is extremely significant.**

Different from SSL on other domains like computer vision and natural language processing, SSL on graphs has an exclusive background, design ideas, and taxonomies. Here are some examples and surveys which are available for [reference](https://arxiv.org/abs/2103.00111).

## Interesting area about topic
After doing some researches about self-supervision on graph data, there is a tyoe of algorithm called PULSE which interests me so much. PULSE(Self-Supervised Photo Upsampling via Latent Space Exploration) aims to search the outputs of a generative model for high-resolution images that are perceptually realistic and downscale correctly by given a low-resolution input image. In the research, it can get a high-resolution image from a corresponding low-resolution input which means we can transform blurry images into sharp, realistic images. Especially nowadays, as resolution in our daily electrical device has increased over recent years, humans' demand for sharp images and high-resolution photo has surged. So it arises my interest in such research which can do great jobs on image super-resolution. 

However, it still has some problems because of its generally applicable. It is difficult to obtain high-resolution images in some areas such as medicine, astronomy, microscopy and satellite imagery due to issues of cost, hardware restriction, or memory limitations.

## Open Source exploring
Through reading the paper link: https://arxiv.org/pdf/2003.03808.pdf, we can know the method using in previous time called MSE. As MSE will blur out the detailed areas of the image at the same time, so MSE should not only be used to measure the super-resolution effect. In order to make up for MSE lost，this [article](https://arxiv.org/pdf/2003.03808.pdf) proposes a new super-resolution mode, it aims to find the image that is actually located on the natural picture manifold space and to ensure that the found image can be correctly downsampled to be the original LR image. 

Based on the research, there are currently two main trends we can explore: 
1. Optimizing the average pixel distance between SR and HR. 
2. Doing more focus on perceived quality.

And here are the project which covers the topic：https://github.com/adamian98/pulse

