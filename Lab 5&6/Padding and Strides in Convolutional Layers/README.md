🧠 CNN Padding & Stride Experiments (MNIST)

This project explores how padding and stride configurations affect the performance of Convolutional Neural Networks (CNNs) when classifying handwritten digits from the MNIST dataset.

The notebook runs multiple CNN experiments using different padding strategies and stride values and compares their impact on:

Model accuracy

Training time

Feature map behavior

Parameter count

📌 Project Overview

Convolutional Neural Networks use filters to extract spatial features from images. Two key hyperparameters in convolution layers are:

1️⃣ Padding

Padding determines how the borders of the image are handled during convolution.

Types used in this experiment:

Same Padding

Keeps the output size equal to the input size.

Preserves edge information.

Valid Padding

No padding applied.

Output feature maps shrink after convolution.

2️⃣ Stride

Stride determines how far the convolution filter moves at each step.

Stride values tested:

Stride = 1 → detailed feature extraction

Stride = 2 → faster downsampling

Stride = 3 → aggressive spatial reduction

🧪 Experiments Conducted

The following configurations were tested:

Experiment	Padding	Stride
Baseline	same	1
No Padding	valid	1
Downsample	same	2
Downsample	valid	2
Aggressive Downsample	same	3

Each experiment trains a CNN on MNIST and records:

Test accuracy

Validation accuracy

Training time

Model parameters

🏗 CNN Architecture

The model architecture used for experiments:

Input (28x28x1)
        │
Conv2D (32 filters)
        │
MaxPooling
        │
Conv2D (64 filters)
        │
MaxPooling
        │
Flatten
        │
Dense (128)
        │
Dropout
        │
Dense (10 Softmax)
📊 Dataset

Dataset used:

MNIST Handwritten Digit Dataset

70,000 grayscale images

Image size: 28 × 28

Classes: 10 digits (0–9)

Split:

Training: 60,000 images

Testing: 10,000 images

🔍 Feature Map Visualization

The notebook also visualizes CNN feature maps from the first convolutional layer.

This helps understand how filters detect:

Edges

Strokes

Digit shapes

Texture patterns

Example visualizations show the activation maps produced by different filters.

⚙️ Technologies Used

Python

TensorFlow / Keras

NumPy

Matplotlib

Jupyter Notebook

▶️ How to Run
1️⃣ Install dependencies
pip install tensorflow numpy matplotlib
2️⃣ Run the notebook

Open the notebook:

Padding&Strides_CNN.ipynb

Run all cells.

📈 Expected Results

Typical observations:

Configuration	Accuracy	Notes
Same + Stride 1	Highest	Best feature preservation
Valid + Stride 1	Slightly lower	Edge information lost
Stride 2	Faster training	Slight accuracy drop
Stride 3	Fastest	Too much information lost
🧠 Key Learning Outcomes

This project demonstrates:

Impact of padding on feature preservation

Effect of stride on spatial resolution

Trade-off between accuracy and computational efficiency

Visualization of CNN feature extraction

🚀 Real-World Applications

Understanding padding and stride is important for designing CNNs used in:

Image classification

Object detection

Medical imaging

Autonomous vehicles

Facial recognition

Video analytics

📂 Project Structure
Padding-Strides-CNN/
│
├── Padding&Strides_CNN.ipynb
└── README.md
👨‍💻 Author

Computer Vision & Deep Learning experiment exploring CNN architectural parameters.
