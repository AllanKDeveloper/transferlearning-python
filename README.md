# Citrus Leaves Dataset

## Description

The Citrus Leaves dataset consists of 594 images of citrus leaves categorized into four labels: Black Spot, Canker, Greening, and Healthy. The images are in PNG format with a resolution of 256x256 pixels. The original dataset contained 759 images of citrus fruits and leaves, but images with the Melanose label were excluded due to their small count and the presence of non-leaf images in the same directory.

The dataset is intended for image classification tasks, particularly for training machine learning models to classify different types of citrus leaf diseases.

- **Labels**:
  - Black Spot
  - Canker
  - Greening
  - Healthy

## Dataset URL

[Dataset on Mendeley](https://data.mendeley.com/datasets/3f83gxmv57/2)

## License

This dataset is licensed under the [Creative Commons Attribution 4.0 International License (CC BY 4.0)](http://creativecommons.org/licenses/by/4.0).

## Homepage

[Dataset Homepage](https://data.mendeley.com/datasets/3f83gxmv57/2)

## Source Code

The source code for the Citrus Leaves dataset can be found under `tfds.image_classification.CitrusLeaves`.

## Versions

- **0.1.1**: Initial release of the Citrus Leaves dataset.
- **0.1.2** (default): Update of the website URL.

## Dataset Information

- **Download Size**: 63.87 MiB
- **Dataset Size**: 37.89 MiB
- **Auto-cached**: Yes

### Splits

| Split | Examples |
|-------|----------|
| 'train' | 594 |

### Features

The dataset consists of the following features:

- `image`: An image of a citrus leaf in PNG format, with shape `(256, 256, 3)` and dtype `uint8`.
- `image/filename`: The filename of the image, represented as a string.
- `label`: The label assigned to the image, represented as a class label with dtype `int64`. There are 4 possible class labels: 0 for Black Spot, 1 for Canker, 2 for Greening, and 3 for Healthy.

### Feature Structure

```python
FeaturesDict({
    'image': Image(shape=(256, 256, 3), dtype=uint8),
    'image/filename': Text(shape=(), dtype=string),
    'label': ClassLabel(shape=(), dtype=int64, num_classes=4),
})
```

### Supervised Keys

The dataset is structured for supervised learning with the following keys:
- ('image', 'label')

## Example Usage

You can load the dataset using TensorFlow Datasets:

```python
import tensorflow_datasets as tfds

# Load the Citrus Leaves dataset
dataset, info = tfds.load('citrus_leaves', with_info=True)

# Inspect the dataset information
print(info)
```

## Visualization

You can visualize the dataset using `tfds.show_examples` to display random images and their corresponding labels.

```python
import tensorflow_datasets as tfds

# Show examples from the Citrus Leaves dataset
dataset, info = tfds.load('citrus_leaves', with_info=True)
tfds.show_examples(dataset['train'], info)
```

## Transfer Learning Example

For a hands-on example of using the Citrus Leaves dataset with Transfer Learning, you can refer to the [Transfer Learning Notebook in Colab](https://colab.research.google.com/github/kylemath/ml4a-guides/blob/master/notebooks/transfer-learning.ipynb).

## Additional Resources

- [TensorFlow Dataset Catalog](https://www.tensorflow.org/datasets/catalog/citrus_leaves)
- [Citrus vs. Dogs Dataset](https://www.microsoft.com/en-us/download/details.aspx?id=54765)

## Contributing

Feel free to fork, modify, and submit pull requests. Please ensure your contributions adhere to the dataset's license and maintain the structure as outlined.
