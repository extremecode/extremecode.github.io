# Data Manipulation

## steps of ML

* Data Collection: The process of extracting raw datasets for the machine learning task. This data can come from a variety of places, ranging from open-source online resources to paid crowdsourcing. The first step of the machine learning process is arguably the most important. If the data you collect is poor quality or irrelevant, then the model you train will be poor quality as well.

* Data Processing and Preparation: Once you’ve gathered the relevant data, you need to process it and make sure that it is in a usable format for training a machine learning model. This includes handling missing data, dealing with outliers, etc.

* Feature Engineering: Once you’ve collected and processed your dataset, you will likely need to transform some of the features (and sometimes even drop some features) in order to optimize how well a model can be trained on the data.

* Model Selection: Based on the dataset, you will choose which model architecture to use. This is one of the main tasks of industry engineers. Rather than attempting to come up with a completely novel model architecture, most tasks can be thoroughly performed with an existing architecture (or combination of model architectures).

* Model Training and Data Pipeline: After selecting the model architecture, you will create a data pipeline for training the model. This means creating a continuous stream of batched data observations to efficiently train the model. Since training can take a long time, you want your data pipeline to be as efficient as possible.

* Model Validation: After training the model for a sufficient amount of time, you will need to validate the model’s performance on a held-out portion of the overall dataset. This data needs to come from the same underlying distribution as the training dataset, but needs to be different data that the model has not seen before.

* Model Persistence: Finally, after training and validating the model’s performance, you need to be able to properly save the model weights and possibly push the model to production. This means setting up a process with which new users can easily use your pre-trained model to make predictions.

* We don't have better algorithms than anyone else; we just have more data."

#DML
When we deal with numeric data, the best Python library to use is NumPy. The NumPy library allows us to perform many operations on numeric data, and convert the data to more usable forms.

```markdown
import numpy as np  # import the NumPy library

# Initializing a NumPy array
arr = np.array([-1, 2, 5], dtype=np.float32)

# Print the representation of the array
print(repr(arr))


array([-1.,  2.,  5.], dtype=float32)

```

Numpy-
# Will result in a ValueError: If we uncomment line int32 and run again.
#np.array([np.nan, 1, 2], dtype=np.int32)
print(repr(np.array([np.nan, 1, 2], dtype=np.float32)))
special values
np.nan
np.inf
# Will result in a OverflowError: If we uncomment below line  and run again.
np.array([np.inf, 3], dtype=np.int32)


A. Ranged data#
While np.array can be used to create any array, it is equivalent to hardcoding an array. This won't work when the array has hundreds of values. Instead, NumPy provides an option to create ranged data arrays using np.arange. The function acts very similar to the range function in Python, and will always return a 1-D array.

```markdown
arr = np.arange(5)
print(repr(arr))

arr = np.arange(5.1)
print(repr(arr))

arr = np.arange(-1, 4)
print(repr(arr))

arr = np.arange(-1.5, 4, 2)
print(repr(arr))

array([0, 1, 2, 3, 4])
array([0., 1., 2., 3., 4., 5.])
array([-1,  0,  1,  2,  3])
array([-1.5,  0.5,  2.5])


```


https://drive.google.com/file/d/15mYwCuoqkEaKNwpvPKXfUMU21hGcf3rC/view?usp=sharing

Venu Gopalhttps://drive.google.com/file/d/1CD2XlL3deHMeKB8YG_wzru-kf6mg2BMX/view?usp=sharing
02:29 PM
VG
Venu Gopalhttps://drive.google.com/file/d/18XlUmj03J1jJCwnW0mW3iRU7kD3VWrdh/view?usp=sharing
02:29 PM
VG
Venu Gopalhttps://drive.google.com/file/d/1pVWZ31621DtLk4aCsw3VJ6u5tEwenZY2/view?usp=sharing
02:30 PM
VG
Venu Gopalhttps://drive.google.com/file/d/1X0iQ7015ZDcwAyvgfEOanipLZO19D3Yl/view?usp=sharing
02:30 PM

