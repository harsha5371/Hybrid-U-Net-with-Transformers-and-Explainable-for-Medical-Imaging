Technologies & Libraries Used:

Core Libraries:

TensorFlow / Keras – Deep learning framework segmentation_models – For building U-Net-like architectures OpenCV, scikit-image – Image processing and transformations NumPy, Pandas – Numerical operations and data handling

Medical Imaging:

Nibabel – Reading .nii medical image formats Nilearn – Visualization of neuroimaging data

Explainable AI (XAI):

Grad-CAM – Visual explanation for model decision-making

Model Architecture: The model is designed by fusing:

VGG19 as a pre-trained encoder, extracting deep spatial features U-Net-style decoder, reconstructing the segmentation mask with skip connections Vision Transformer (ViT) blocks in the bottleneck to enhance long-range feature dependencies and attention mechanisms

This combination allows the model to leverage:

Local texture details via CNN (VGG19) Global context and feature enhancement via Transformers High-resolution segmentation through U-Net's architecture

Dataset: Dataset: BraTS 2020 Source: Brain Tumor Segmentation Challenge Format: .nii MRI scans with corresponding segmentation masks Modalities used: Can include T1, T2, FLAIR, etc. Tumor Regions: Whole Tumor (WT), Tumor Core (TC), and Enhancing Tumor (ET)

Preprocessing:

Converted 3D .nii volumes into 2D slices Normalized image intensities using MinMaxScaler Resized images to uniform shape (typically 128x128 or 256x256) Applied data augmentation like flipping, rotation for generalization
