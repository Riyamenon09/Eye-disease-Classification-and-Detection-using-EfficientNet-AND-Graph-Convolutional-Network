# Eye-disease-cClassification-and-Detection-using-EfficientNet-AND-Graph-Convolutional-Network
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

🔍 EfficientNetB0 Model Architecture 🔹 ImageNet Pretrained

To extract deep features, set include_top=False.
utilized to create embeddings from previously processed photos.
EfficientNet features are transformed into nodes for the Graph Convolutional Network (GCN).
Similarities in space or statistics are used to define edges.
This graph is used by GCN to categorize illnesses.
This dual-model pipeline connects graph-based reasoning with image-level processing.
