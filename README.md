# Deep Image Search - AI-Based Image Search Engine
<p align="center"><img src="https://github.com/TechyNilesh/DeepImageSearch/blob/main/logo/deep%20image%20search%20logo%20New.png?raw=true" alt="Brain+Machine" height="218" width="350"></p>

**Deep Image Search** is an AI-based image search engine that includes **deep transfer learning features Extraction** and **tree-based vectorized search technique.**

![Generic badge](https://img.shields.io/badge/AI-Advance-green.svg) ![Generic badge](https://img.shields.io/badge/Python-v3-blue.svg) ![Generic badge](https://img.shields.io/badge/pip-v3-red.svg)  ![Generic badge](https://img.shields.io/badge/TensorFlow-v2-orange.svg) ![Generic badge](https://img.shields.io/badge/Annoy-latest-green.svg) [![Downloads](https://static.pepy.tech/personalized-badge/deepimagesearch?period=month&units=international_system&left_color=grey&right_color=brightgreen&left_text=Downloads)](https://pepy.tech/project/deepimagesearch)

<h2><img src="https://cdn2.iconfinder.com/data/icons/artificial-intelligence-6/64/ArtificialIntelligence9-512.png" alt="Brain+Machine" height="38" width="38"> Creators </h2>

### [Nilesh Verma](https://nileshverma.com "Nilesh Verma")

## Features
- Faster Search **O(logN)** Complexity.
- High Accurate Output Result.
- Best for Implementing on python based web application or APIs.
- Best implementation for College students and freshers for project creation.
- Applications are Images based E-commerce recommendation, Social media and other image-based platforms that want to implement image recommendation and search.

## Installation

This library is compatible with both *windows* and *Linux system* you can just use **PIP command** to install this library on your system:

```shell
pip install DeepImageSearch
```

If you are facing any VS C++ 14 related issue in windows during installation, kindly refer to following solution: [Pip error: Microsoft Visual C++ 14.0 is required](https://stackoverflow.com/questions/44951456/pip-error-microsoft-visual-c-14-0-is-required "Pip error: Microsoft Visual C++ 14.0 is required")

## How To Use?

We have provided the **Demo** folder under the *GitHub repository*, you can find the example in both **.py** and **.ipynb**  file. Following are the ideal flow of the code:

### 1. Importing the Important Classes
There are three important classes you need to load **LoadData** - for data loading, **Index** - for indexing the images to database/folder, **SearchImage** - For searching and Plotting the images

```python
# Importing the proper classes
from DeepImageSearch import Index,LoadData,SearchImage
```

### 2. Loading the Images Data

For loading the images data we need to use the **LoadData** object, from there we can import images from the CSV file and Single/Multiple Folders.

```python
# load the Images from the Folder (You can also import data from multiple folders in python list type)
image_list = LoadData().from_folder(['images','wiki-images'])
# Load data from CSV file
image_list = LoadData().from_csv(csv_file_path='your_csv_file.csv',images_column_name='column_name)
```
### 3. Indexing and Saving The File in Local Folder

For faster retrieval we are using tree-based indexing techniques for Images features, So for that, we need to store meta-information on the local path **[meta-data-files/]** folder.

```python
# For Faster Serching we need to index Data first, After Indexing all the meta data stored on the local path
Index(image_list).Start()
```
### 3. Searching

Searching operation is performed by the following method:

```python
# for searching, you need to give the image path and the number of the similar image you want
SearchImage().get_similar_images(image_path=image_list[0],number_of_images=5)
```
you can also plot some similar images for viewing purpose by following the code method:

```python
# If you want to plot similar images you can use this method, It will plot 16 most similar images from the data index
SearchImage().plot_similar_images(image_path = image_list[0])
```

## Complete Code

```python
# Importing the proper classes
from DeepImageSearch import Index,LoadData,SearchImage
# load the Images from the Folder (You can also import data from multiple folder in python list type)
image_list = LoadData().from_folder(['images','wiki-images'])
# For Faster Serching we need to index Data first, After Indexing all the meta data stored on the local path
Index(image_list).Start()
# for searching you need to give the image path and the number of similar image you want
SearchImage().get_similar_images(image_path=image_list[0],number_of_images=5)
# If you want to plot similar images the you can use this method, It will plot 16 most similar images from the data index
SearchImage().plot_similar_images(image_path = image_list[0])
```

## License



    MIT License
    
    Copyright (c) 2021 Nilesh Verma
    
    Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

### Please do STAR the repository, if it helped you in anyway.

**More cool features will be added in future. Feel free to give suggestions, report bugs and contribute.**
