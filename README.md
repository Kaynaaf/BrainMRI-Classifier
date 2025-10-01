# Tumor-Classification-and-sensitivity-maps
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1SfK9d2In3JHDvyXH4jpwznVGEG_wXRuQ?usp=sharing)

[![Model on HF](https://huggingface.co/datasets/huggingface/badges/resolve/main/model-on-hf-md.svg)](https://huggingface.co/Kaynaaf/BrainMRI-Classifier)

[![Dataset on HF](https://huggingface.co/datasets/huggingface/badges/resolve/main/dataset-on-hf-md.svg)](https://huggingface.co/datasets/Kaynaaf/Brain-Tumour-MRI)




## What's the project about

I created a custom keras model and trained it for image classification. The dataset I selected was of MRI scans of different types of tumours in the Brain.

with 4 classes in total, including a control one, the dataset contained ~7000 images with a 80-20 split.

I used the model to predict whether a certain type of tumour was present or if no tumour was present at all.

Another thing I implemented was explaining the predictions using a visual aid.
For that I implemented a function to perform occlusion sensitivity analysis, a technique that generates a heatmap showing important areas of the image relevant to the model's prediction of any image.


## Model Evaluation

### Classification Report

| Class       | Precision | Recall | F1-Score | Support |
|-------------|-----------|--------|----------|---------|
| Glioma      | 0.96      | 0.87   | 0.91     | 300     |
| Meningioma  | 0.84      | 0.71   | 0.77     | 306     |
| No Tumor    | 0.88      | 1.00   | 0.93     | 405     |
| Pituitary   | 0.93      | 0.99   | 0.96     | 300     |
| **Accuracy**|           |        | **0.90** | 1311    |
| **Macro Avg** | 0.90    | 0.89   | 0.89     | 1311    |
| **Weighted Avg** | 0.90 | 0.90   | 0.90     | 1311    |

The model averaged 90% accuracy on the test set.

### Confusion Matrix
[Confusion matrix](results/cm.png)
