# covid-classification
T1(it only gives correct results if we upload both image and its mask(we can also use t2 for generating that)): a deep learning classifier that takes an x-ray image as the input and
assigns the input image to one of the four classes: COVID-19 positive, Normal, Lung Opacity, Viral Pneumonia.

T2(okay but needs to get optimized): an image segmentation network to segment the left and right lungs from the x-ray images.
Encoder: ResNet50 extracts rich features from images.
Decoder: Custom U-Net decoder upsamples features to original resolution.
Skip Connections: Preserve spatial information, improving segmentation accuracy.
**Binary Cross-Entropy (BCE):**
Measures the difference between the predicted probabilities and the true binary labels.
Ensures that the model outputs probabilities close to the true labels.
**Dice Loss:**
Measures the overlap between the predicted segmentation and the ground truth segmentation.
Directly maximize the intersection over the union of the predicted and true segmentations, which is useful for imbalanced classes.

rough is just for testing t1 and t2
