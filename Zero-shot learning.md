The survey of zero-shot learning.

### Some datasets(from [this](http://www.yugangjiang.info/publication/SPM18-survey.pdf))
- **AwA([Animals with Attributes](https://cvml.ist.ac.at/AwA/))**
  - The Animals with Attributes (AwA) data set consists of the 50 Osher-son/Kemp animal category images collected online. There are 30,475 images with at least 92 examples of each class. Seven different feature types are provided: RGB color histograms, scaleinvariant feature transform (SIFT), rgSIFT, pyramid histogram of oriented gradients, speeded up robust features, local self-similarity histograms, and DeCaf. The AwA data set defines 50 classes of animals, and 85 associated attributes (such as “furry” and “has claws”). For the consistent evaluation of attribute-based object classification methods, the AwA data set defined ten test classes: chimpanzee, giant panda, hippopotamus, humpback whale, leopard, pig, raccoon, rat, Persian cat, and seal. The 6,180 images of those classes are taken as the test data, whereas the 24,295 images of the remaining 40 classes can be used for training. Since the images in AwA are not available under a public license, [Xian et al.](https://arxiv.org/pdf/1703.04394.pdf) introduced another new zero-shot learning data set, [AWA2](https://cvml.ist.ac.at/AwA2/), which includes 37,322 publicly licensed and released images from the same 50 classes and 85 attributes as AwA.
  
- **CUB([Caltech-UCSD Birds-200-2011](http://www.vision.caltech.edu/visipedia/CUB-200-2011.html))**
  - CUB-200-2011 contains 11,788 images of 200 bird classes. This is a more challenging data set than AwA—it is designed for fine-grained recognition and has more classes but fewer images. All images are annotated with bounding boxes, part locations, and attribute labels. Images and annotations were filtered by multiple users of AMT. CUB-200-2011 is used as the benchmark data set for mul- ticlass categorization and part localization. Each class is annotated with 312 binary attributes derived from the bird species ontology. A typical setting is to use 150 classes as auxiliary data, holding out 50 as target data, which is the setting adopted in [Akata et al.](https://arxiv.org/pdf/1503.08677.pdf)

- **SUN(SUN attribute data set)**
  - The SUN attribute data set is a subset of the [SUN database](https://groups.csail.mit.edu/vision/SUN/) for fine-grained scene categorization, and it has 14,340 images from 717 classes (20 images per class). Each image is annotated with 102 binary attributes that describe the scenes’ material and surface properties as well as lighting conditions, functions, affordances, and general image layout.
  
- **FLO([Oxford 102 flower data set](http://www.robots.ox.ac.uk/~vgg/data/flowers/))**
  - The Oxford 102 flower data set is a collection of 102 groups of flowers, each with 40–256 flower images and a total of 8,189 images. The flowers were chosen from the common flower spe- cies in the United Kingdom. Elhoseiny et al. generated textual descriptions for each class of this data set.

### Some approaches
- ALE
  - Z.Akata, F.Perronnin, Z.Harchaoui, and C.Schmid: [Label-embedding for image classification](https://arxiv.org/pdf/1503.08677.pdf). TPAMI, 2016.
- DeViSE
  - A.Frome, G.S.Corrado, J.Shlens, S.Bengio, J.Dean, M.A.Ranzato, and T.Mikolov.Devise: [A deep visual-semantic embedding model](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/41473.pdf). In NIPS, 2013.
- SJE
  - Z.Akata, S.Reed, D.Walter, H.Lee, and B.Schiele: [Evaluation of output embeddings for fine-grained image classification](https://arxiv.org/pdf/1409.8403.pdf). In CVPR, 2015.
- ESZSL
  - B.Romera-Paredes and P.H.Torr: [An embarrassingly simple approach to zero-shot learning](http://proceedings.mlr.press/v37/romera-paredes15.pdf). ICML, 2015.
- LATEM
  - Y.Xian, Z.Akata, G.Sharma, Q.Nguyen, M.Hein, and B.Schiele: [Latent embeddings for zero-shot classification](https://arxiv.org/pdf/1603.08895.pdf). In CVPR, 2016.
  - Y.Xian, Z.Akata, G.Sharma, Q.Nguyen, M.Hein, and B.Schiele: [Latent embeddings for zero-shot classification](https://arxiv.org/pdf/1603.08895.pdf). In CVPR, 2016.
  - Y.Xian, Z.Akata, G.Sharma, Q.Nguyen, M.Hein, and B.Schiele: [Latent embeddings for zero-shot classification](https://arxiv.org/pdf/1603.08895.pdf). In CVPR, 2016.
  
  
 ### Some articles
 - [Recent Advances in Zero-Shot Recognition: Toward data-efficient understanding of visual content](http://www.yugangjiang.info/publication/SPM18-survey.pdf)
