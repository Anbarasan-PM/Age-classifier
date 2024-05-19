# Age and Gender prediction Model (Trained on Indian Faces)

This is the Age and Gender prediction model built using Convolutional Neural Networks in Python.
The model is built on the basis of Research Paper by [Gil Levi and Tal Hassner](https://talhassner.github.io/home/publication/2015_CVPR "Age and Gender Classification Using Convolutional Neural Networks"). The neural architecture is built as written in the paper with slight modifications according to the dataset for better perfomance.

The dataset used are [UTKFace Dataset](https://susanqq.github.io/UTKFace/ "Large Scale Face Dataset") and [FairFace Dataset](https://arxiv.org/abs/1908.04913 "FairFace: Face Attribute Dataset for Balanced Race, Gender, and Age") out of which Indian Race faces were seperated and the model was trained with.



## Frameworks used

-   Tensorflow &nbsp;&nbsp; `pip install tensorflow`
-   Numpy &nbsp;&nbsp; `pip install numpy`
-   Keras &nbsp;&nbsp; `pip install keras`
-   Pillow &nbsp;&nbsp; `pip install pillow`

## Performance of model

The output of the model consists of 2 classes for Gender Prediction, namely `Male` and `Female` and 9 classes for the Age Prediction, which are `(0-2), (3-9), (10-19), (20-29), (30-39), (40-49), (50-59), (60-69), (70+)`. The table below shows the performance of model when tested on `13835` images containing Indian faces only.

**Naming Convention used**: _True_ or _False_ represent whether the prediction is Right or Wrong Respectively. _Male_ or _Female_ represents what the model predicted.
For eg: _False Female_ means the model predicted Wrong and Prediction was Female. Which means actually it was Male.

| Age Group   | True Male | False Male | True Female | False Female |
| ----------- | --------- | ---------- | ----------- | ------------ |
| **(0-2)**   | 55        | 32         | 88          | 12           |
| **(3-9)**   | 561       | 221        | 793         | 138          |
| **(10-19)** | 784       | 216        | 645         | 70           |
| **(20-29)** | 1701      | 222        | 1484        | 53           |
| **(30-39)** | 1157      | 166        | 1752        | 44           |
| **(40-49)** | 641       | 105        | 1062        | 26           |
| **(50-59)** | 382       | 65         | 645         | 22           |
| **(60-69)** | 190       | 56         | 249         | 6            |
| **(70+)**   | 90        | 28         | 69          | 5            |

The Accuracy achieved in Gender Prediction is `88.2%`
