# ResNet50_BrainTumour
# Brain Tumor Detection Using ResNet-50

## Project Overview

This project focuses on detecting brain tumors from MRI images using a Convolutional Neural Network (CNN) with the ResNet-50 architecture. The goal is to accurately classify MRI images into four categories: Glioma Tumor, Meningioma Tumor, No Tumor, and Pituitary Tumor.

### Dataset

The dataset used for this project is sourced from Kaggle. It consists of MRI images organized into two main folders:

- `Training`: Contains images for training the model.
  - Subfolders: `glioma_tumor`, `meningioma_tumor`, `no_tumor`, `pituitary_tumor`
- `Testing`: Contains images for evaluating the model.
  - Subfolders: `glioma_tumor`, `meningioma_tumor`, `no_tumor`, `pituitary_tumor`

### Model Architecture

The project utilizes the ResNet-50 architecture, which is known for its deep residual learning framework. ResNet-50 is chosen for its effective handling of vanishing gradient problems through skip connections (identity blocks) and its ability to learn complex features.

#### ResNet-50 Architecture

- **Identity Block**: A residual block where the input is added to the output of a series of convolutional layers. This helps in preserving information across layers and tackling the vanishing gradient problem.
  
- **Convolution Block**: A residual block that includes a convolutional layer with a stride to change the dimensions of the feature maps. It is followed by batch normalization and a ReLU activation.

### Implementation

The implementation involves the following key steps:

1. **Data Preparation**: Load and preprocess the MRI images from the Kaggle dataset. Images are resized to 150x150 pixels and normalized.

2. **Model Building**: Use the ResNet-50 architecture for the CNN model. The model is compiled with categorical crossentropy loss and Adam optimizer.

3. **Training**: Train the model using the training set with validation to monitor performance.

4. **Evaluation**: Evaluate the model on the test set to assess its performance.

5. **Visualization**: Plot training and validation accuracy, loss curves, precision-recall curves, and confusion matrices.

### Outputs

- **Training and Validation Accuracy/Loss Curves**: Visualize how the model's performance improves over epochs.
- **Precision, Recall, F1-Score**: Detailed metrics for each class.
- **ROC Curves**: Performance of the model across different classes.
- **Grad-CAM Heatmaps**: Visualize areas of the input images where the model focuses.
- **Confusion Matrix**: Show the classification results and misclassifications.

### Conclusion

The project demonstrates the effectiveness of the ResNet-50 architecture in classifying brain tumors from MRI images. By leveraging the deep residual learning approach, the model achieves improved accuracy and robustness. The visualization plots provide insights into the model's performance and help in identifying potential areas for further improvement.

### Diagrams

- **ResNet-50 Architecture**: ![Screenshot 2024-08-03 161846](https://github.com/user-attachments/assets/50b8a1fa-0deb-43bf-9933-66416cd99766)
 
- **Identity Block and Convolution Block**: ![Screenshot 2024-08-03 161828](https://github.com/user-attachments/assets/b03b3455-8c31-4b0d-b67a-9dfe33557fcf)
![Screenshot 2024-08-03 161838](https://github.com/user-attachments/assets/56118af7-fc6e-48ca-beb5-5d0f9876b869)


- **Output Visualization**:
 ![Screenshot 2024-08-03 162138](https://github.com/user-attachments/assets/f01c8329-1c45-4bc1-aecd-ef8156d032eb)
 ![Screenshot 2024-08-03 161947](https://github.com/user-attachments/assets/99fd6c08-c5c3-4c2e-84d4-0edb69ef153d)
![Screenshot 2024-08-03 162041](https://github.com/user-attachments/assets/3d774d83-0836-46e0-90cc-16cbe3d49e97)
![Screenshot 2024-08-03 162059](https://github.com/user-attachments/assets/59ed140e-b5e9-4247-a8fe-83a0b1cb9f9b)


### Installation and Usage

To run this project, ensure you have the following libraries installed:

```bash
pip install tensorflow numpy matplotlib scikit-learn opencv-python
