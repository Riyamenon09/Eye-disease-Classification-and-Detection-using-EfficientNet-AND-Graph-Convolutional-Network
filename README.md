# Eye-disease-Classification-and-Detection-using-EfficientNet-AND-Graph-Convolutional-Network
This project is an attempt at diagnosis of serious eye diseases through fundus images and deep learning models. EfficientNet (to extract strong image features) and Graph Convolutional Networks (GCN) (to model spatial relationships) are combined to enhance classification accuracy for four classes:

*Diabetic Retinopathy

*Cataract

*Glaucoma

*Normal

Blindness and visual impairment are among the major causes. Early diagnosis through AI-based screening can significantly lower morbidity. Unlike CNN-only pipelines, this combination is a hybrid method that leverages CNNs for local image features and GCNs for the structural relationships between them, leading to more sound and explainable learning.

Images are retrieved from different folders related to the disease classes. Preprocessing involves:
Grayscale
Contrast enhancement
Channel-wise wavelet decomposition (LL, HL, LH, HH bands)
Image resizing to 224x224
Preprocessing of each image conditionally only if it is not already enhanced.

Model Architecture

-> EfficientNetB0
Pretrained on ImageNet

include_top=False to extract deep features

Used for generating embeddings from preprocessed images

-> Graph Convolutional Network (GCN)
Features from EfficientNet are converted into nodes

Edges are defined based on spatial or statistical similarities

GCN operates on this graph to classify diseases

This dual-model pipeline bridges image-level processing with graph-based reasoning.
