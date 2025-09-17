This project focuses on automated diagnosis of eye diseases from fundus images using a hybrid deep learning pipeline that integrates EfficientNet for image feature extraction and Graph Convolutional Networks (GCN) for modeling structural relationships. The system classifies images into four categories: Diabetic Retinopathy, Cataract, Glaucoma, and Normal, and further performs severity grading to assess disease progression.
Key Contributions

Image Preprocessing: Applied grayscale conversion, contrast enhancement, wavelet decomposition, and image resizing to enhance discriminative features.

Hybrid Model Architecture:

EfficientNetB0 (pretrained on ImageNet, feature extractor) generates deep embeddings from fundus images.

Graph Convolutional Network (GCN) processes these embeddings by constructing a graph where nodes represent features and edges capture spatial/statistical relationships.

Graph Coarsening and Refining techniques were implemented to reduce redundant nodes (coarsening) and progressively restore fine-grained details (refining), improving efficiency and capturing both global and local disease patterns.

Severity Grading: Developed a grading algorithm that integrates clinical factors (disease-specific risk indicators) with image-based features to automatically quantify disease severity levels.

Outcome

This dual-model pipeline combines CNN-based local feature extraction with graph-based relational reasoning and hierarchical graph processing (coarsening/refining). The approach improves classification accuracy, robustness to noise, and provides a more clinically interpretable severity assessment.
