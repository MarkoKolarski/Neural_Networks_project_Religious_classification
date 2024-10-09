# Religious Classification Using Exploratory Data Analysis and Neural Networks

## Project Overview

This research report presents the application of exploratory data analysis and neural networks for classifying countries based on their dominant religion, focusing on features of their national flags and basic geopolitical attributes. We aim to investigate the correlation between the design elements of a flag and the dominant religion of the respective country. The methods include the implementation of convolutional neural networks (CNN) and multiple neural networks to analyze both visual and numerical data, providing a comprehensive model of religious classification.

---

## 1. Introduction

### 1.1. Research Focus

The primary focus of this research is to classify the dominant religion of a country by analyzing the characteristics of its flag and geopolitical features using neural networks. The project explores whether the appearance of a flag is indicative of the dominant religion of a country and aims to identify the most relevant features for this prediction.

### 1.2. Research Objectives

- **Exploring the relationship between flag design and dominant religion.**
- **Identifying key characteristics for accurate classification.**
- **Using exploratory analysis to derive preliminary insights.**
- **Building CNN models to process visual data of flags.**
- **Adjusting pre-trained models such as MobileNetV2 for comparison.**
- **Implementing a multi-layer neural network for numeric data from a CSV file.**

### 1.3. Research Tasks

1. Collect and preprocess a comprehensive dataset of countries, including their flags and geopolitical attributes.
2. Perform exploratory data analysis (EDA) to investigate data patterns and trends.
3. Develop and train a convolutional neural network (CNN) from scratch.
4. Adapt a pre-trained CNN model (MobileNetV2) for classification.
5. Compare the performance of the scratch-built and pre-trained models.
6. Implement a separate multi-layer neural network to handle numerical data for classification.
7. Analyze and consolidate findings into global insights.

### 1.4. Expected Outcomes

- Identification of the most significant features for religious classification based on country flags.
- Construction of prediction models with measurable accuracy.
- Insights into relationships between flag design and religion.

---

## 2. Methodology

### 2.1. Dataset

The dataset contains information about various countries and their flags. It includes basic geopolitical features such as continent, area, population, language, and dominant religion. The flag-related features include color variety, design elements (such as stripes, circles, crosses, and stars), and the dominant hue of the flag. The dataset covers 177 countries with 30 columns, offering a rich source of visual and numerical data.

In addition to the CSV file, we compiled a dataset of flag images from the year 1986 to match the CSV data. The dataset contains images of country flags that needed cleaning and preparation before analysis.

### 2.2. Previous Research

This dataset was sourced from the University of California, Irvine. Unlike popular datasets like those on Kaggle, we found no prior studies related to this dataset or similar research on the web.

### 2.3. Research Methods

Our research methods include exploratory data analysis (EDA), CNN development, and the use of pre-trained models. The data preparation process involved several key steps:

- **Data Cleaning**: Images were gathered from a 1986 flag dataset. We wrote a Python script to rename files, remove unnecessary images, and map file names to country names in the CSV file.
- **Dataset Integration**: We integrated the flag images into the main dataset by adding image file paths as a new column, enabling the combination of visual and numerical data for analysis.

---

## 3. Results

### 3.1. EDA Results

**Ilija's Analysis**: The exploratory analysis produced several charts that showcase significant variable distributions. These results were divided into three sections:

1. **Distribution Analysis**: A series of graphs that show the frequency of variables such as languages spoken, dominant flag colors, and religions. For example, English is the most commonly spoken language, red is the most frequent flag color, and Christian-majority countries are dominant in the dataset. Binary analysis revealed that red and white are the most common flag colors, while orange and black are least represented.
   
2. **Attribute Comparisons**: Analysis showed the relationships between religious groups and flag design elements (e.g., stripes, colors, and symbols). For instance, flags with three vertical stripes are commonly associated with Catholic-majority countries.

3. **Correlation Matrix**: This analysis examined the relationships between numerical variables, revealing patterns such as the tendency for certain symbols (e.g., crosses) to appear more frequently in Christian-majority countries.

### 3.2. CNN Implementation and Results

**Marko's CNN Model**: The custom-built CNN aimed to predict the dominant religion of a country based on flag images. The model's accuracy reached 80% for countries in Africa, with a significant variation in flag design influencing the results. Although the accuracy for the rest of the world was 50%, the model performed better with larger, more diverse datasets.

**Srđan's MobileNetV2 Implementation**: A pre-trained MobileNetV2 model was adapted to the dataset, but it achieved only 20% accuracy for African countries, often predicting ethnic religions inaccurately. Despite the overfitting to the training data, the model’s prediction accuracy for the rest of the world remained low, at 20%.

### 3.3. Multilayer Neural Network

A separate neural network was developed to predict religion based on numerical data from the CSV file. The overall accuracy was around 39%, with a peak of 56%, though this was achieved under conditions of overfitting.

---

## 4. Discussion

**Ilija's Insights**: The first part of the analysis provided a simple overview of the dataset's composition, with clear patterns emerging from the distribution of variables. Further comparisons between flag elements and religions revealed some noteworthy correlations, such as the prevalence of crosses in Christian-majority countries.

**Marko's CNN vs. Srđan's MobileNetV2**: Marko's custom CNN outperformed Srđan's MobileNetV2 in all cases, particularly for African countries, where Marko's model reached an accuracy of 80%. The MobileNetV2 model struggled to differentiate between religions, likely due to its pre-trained nature, not being fine-tuned for this specific dataset.

---

## 5. Conclusion

This research demonstrates the potential for using neural networks to classify countries by religion based on their flag designs and geopolitical features. Although the results were mixed, particularly with pre-trained models, the custom-built CNN showed promising results, especially when working with regional subsets of the data. Future improvements may involve expanding the dataset, further tuning the models, and exploring additional features to enhance prediction accuracy.

---

### Author Contributions

- **Ilija**: Exploratory data analysis, chart creation, result interpretation.
- **Marko**: Custom CNN implementation and performance analysis.
- **Srđan**: MobileNetV2 adaptation and comparison, multilayer neural network development.

---

### References

- Dataset: University of California, Irvine
- Libraries used: TensorFlow, Keras, Matplotlib, Pandas, NumPy
