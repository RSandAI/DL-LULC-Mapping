# DL-LULC-Mapping

## Weights

Model weights are available here : 
https://drive.google.com/drive/folders/1RDQRY-L8LcuNj5nTSRZnSg-on70sJ6x9?usp=sharing

## LAND USE/LAND COVER MAPPING USING DEEP LEARNING METHODS

It contains the summary of the study of İskender Berkay Sür from Istanbul Technical University's undergraduate thesis 'LAND USE/LAND COVER MAPPING USING DEEP LEARNING METHODS' and the notebook and model weights used in Deep Learning studies.

## Summary

Land Use and Land Cover Maps (LULC) are used in many sectors for various purposes. Among these purposes, along with global objectives such as sustainability studies; LULC maps are used in studies in many areas such as city planning, vegetation analysis, natural resources, studies on historical sites, mining areas, natural disaster analysis. For the production of LULC maps, it is currently done with the use of various software and human operators. In the production of these maps, there are various error sources from software and manufacturers. In addition, a rapid change is taking place in the world with the ever-increasing population and technology, and it has become a necessity to update the LULC maps in more areas and more frequently. It is also of great importance that various information, analyzes and estimates that can be extracted from these maps are used within the scope of United Nations (UN) sustainability principles. Satellite images, aerial images and images obtained by various methods are used in the creation of LULC maps. With the images obtained thanks to the RS, the production of LULC maps has accelerated. In addition to this, LULC maps have also created a source for Geographic Information Systems (GIS) data and their use has become widespread. With the increasing abundance of data sources for the creation of LULC maps, and the resolution and quality of the images obtained by IA methods, the speed of creation of LULC maps and the accuracy of the maps created have increased by using Deep Learning (DL) methods, which have shown rapid development in recent years. Convolutional Neural Networks (CNN) architectures such as AlexNET, VGGNET, ViT, DenseNET, UNet, DeeplabV3 are used for visual tasks such as image classification, object recognition and semantic segmentation. CNN consists of 5 important layers, which are convolution, activation, pooling, fully connected layers and dropout layers, and this allows the architectures used to obtain a result product on images more successfully. Studies on this subject have been carried out with various RS data and DL algorithms. Here, the performances of producing LULC maps created with DL algorithms are evaluated with general accuracy, average accuracy, error matrix, weighted accuracy, sensitivity, precision, F1 score, IoU score and kappa statistics. In this context, it is of great importance that the analysis, images and studies obtained as a result of the classification and creation of LULC maps, which are obtained with these algorithms and which are important for the purposes of a global issue such as sustainability, to be used in joint studies and to comply with international standards. . In this context, when we look at the standards, Coordination of Information on the Environment (CORINE) classification, United Nations Geological Survey (USGS) classification and USGS Land Cover Institute (LCI) classifications, which are widely used for classification studies, which are the stages of creating maps, are among the popular classification methods. Based on the findings of this study, LULC maps based on CORINE classification were produced in the Aksu region of Bursa, where approximately 85% of the forest and agricultural lands are located. In the Unet++ architecture, using the Resnext-50 backbone and Adam optimizer with a learning rate of 10-5, a batch rate of 4, and 100 epochs, the lowest Dice Focal Loss was achieved, resulting in an approximate 84% IoU score and 91% F1 score. When evaluated in terms of the environment, cost, and time, the study produced fast, high-performance, and accurate LULC maps. The selection of the most suitable datasets for generating LULC maps through DÖ algorithms, testing the algorithms based on these datasets, subjecting these tests to performance evaluations, and continuing the work with the most accurate results are also of great importance in line with Sustainable Development Goals (SDGs).

## Study Area

The region selected for the dataset is the Aksu region of Bursa province in Turkey, which is the region shown in Figure . The location of this region is 40.18°N, 29.07°E, within the borders of Bursa at an altitude of 150 m. The Aksu region was chosen because it has a variety of agricultural land and forested areas, as well as man-made areas such as urban fabric and mining areas.

![Output](https://github.com/RSandAI/DL-LULC-Mapping/blob/main/Images/Area.png?raw=true)

## Data

In creating the dataset, 4 different spectral bands were combined on a single image. The panchromatic (PAN) image with a resolution of 30 cm and four multi-spectral bands (red, green, blue and near infrared) with a resolution of 2 m were combined with the Pansharp2 algorithm and pan-sharpened images with a resolution of 30 cm were produced with four spectral bands. The data was divided into 419 data for training, 120 data for validation and 60 data for testing, i.e. 70% for training, 20% for validation and 10% for testing. The images are 512* 512 in size. As can be seen in the figure, there are images and masks consisting of 10 different regions, 9 different classes and regions without data. Forest is 44.1%, heterogeneous agricultural areas 26%, no data 12.3%, arable agricultural lands 8.9%, permanent agricultural areas 5.0%, discontinuous urban texture 1%, inland water resources 0.9%, mining-casting and construction sites 0.7%, roads and railways 0.5% and artificial non-agricultural vegetation areas 0.1%.

![Output](https://github.com/RSandAI/DL-LULC-Mapping/blob/main/Images/Data%20Classes.png?raw=true)

##  Thesis Study

Figures Summarize Related Study

![Output](https://github.com/RSandAI/DL-LULC-Mapping/blob/main/Images/Method.png?raw=true)

![Output](https://github.com/RSandAI/DL-LULC-Mapping/blob/main/Images/Test%20Maps.png?raw=true)

## Evaluation

The created ACAE maps were evaluated with IoU score, F1 score, precision, recall and Dice Focal Loss metrics. The graph shows the comparisons.

![Output](https://github.com/RSandAI/DL-LULC-Mapping/blob/main/Images/Metrics.png?raw=true)

# Result

The use of DL methods in the creation of LULUC maps is an effective method in terms of time, cost and even resources. Segmenting the very high resolution satellite images one by one, performing segmentation and evaluating their accuracy by making sense of them and creating maps based on them are comprehensive studies that require time. CNN-based Object-Oriented Image Analysis analysis is of great importance in this context, especially in evaluating the long-term time-dependent change of a region or regions. The most important feature of the Aksu dataset is that it has 44.1% forest and 40.1% agricultural area. This reveals the importance of LULC maps, especially in areas such as fire, natural disasters, urbanization activities that threaten forests and where long-term continuous change needs to be examined and analyzed. When Aksu region is taken as a reference, LULC maps are important in order to end hunger by supporting climate action and terrestrial life and supporting agricultural areas in line with the SDG targets. In this study, the effect of the distribution of the classes in the dataset on segmentation was measured and segmentation was performed by performing CNN-based Object-Oriented Image Analysis on encoder-decoder architectures. Based on the findings of the study, Unet++ architecture, Resnext-50 backbone and Adam optimizer were used to obtain the highest performance and accuracy of the LULC maps in terms of learning rate of 10-5, batch rate of 4, f1 score at 100 epochs, IoU, precision and accuracy, and dice focal loss. It was even possible to eliminate erroneous segmentations due to human factors independent of the real ground masks. With GPUs with higher memory and long-term studies, it is possible to produce much closer to the reality. However, the main goal here is to make a continuous analysis and observation when time, cost and resources are to be worked efficiently. In other words, the use of DL-based models in the preparation and evaluation of LULC maps increases the accuracy and efficiency of the studies in these areas, and based on this, it provides significant progress towards the SDGs.

### References

**İskender Berkay Sür** B. Sc. Thesis (2024)

**Sertel, E., Ekim, B., Osgouei, P. E., & Kabadayi, M. E.** (2022). Land Use and Land Cover Mapping Using Deep Learning Based Segmentation Approaches and VHR Worldview-3 Images_. Remote Sensing, 14_(18), 4558. https://doi.org/10.3390/rs14184558
