# Datasheet: Book Sales Dataset

## Motivation

- **Purpose**: The dataset was created to provide insight into the book sales industry and to enable predictive modeling on book sales based on various features.
- **Creator**: The dataset was created by [Josh Murrey](https://data.world/josh-nbu/books).
- **Funding**: There is no specific information available regarding funding.

## Composition

- **Instances**: The dataset contains information about books, including their sales figures and related metadata. The instances represent individual books.
- **Number of Instances**: The exact number of rows (instances) is not specified here but can be found in the dataset.
- **Missing Data**: Yes, the dataset contains missing data, which was handled during preprocessing. Missing categorical data (such as "Book Name" or "Author") was filled with 'Unknown', and missing numerical data was imputed using the median.
- **Confidential Data**: The dataset contains non-confidential information about books and their authors but may raise privacy concerns related to the inclusion of author names and other metadata depending on legal jurisdiction.

## Collection Process

- **Data Acquisition**: The exact methodology of data acquisition is unknown.
- **Sampling Strategy**: It is not specified if the dataset is a sample of a larger collection.
- **Time Frame**: The dataset was created in **August 2018**, but there is no information on the specific time period over which the data was collected.

## Preprocessing/Cleaning/Labeling

- **Preprocessing**: 
   - **Missing Data Handling**: Categorical features with missing values were filled with 'Unknown'. Missing numerical values were imputed with the median.
   - **Scaling**: All numerical features were standardised using `StandardScaler`.
   - **Encoding**: Categorical features were one-hot encoded, with the `OneHotEncoder` handling unknown categories.
- **Raw Data**: There is no indication that the raw (pre-cleaned) version of the data was saved.

## Uses

- **Possible Uses**: This dataset can be used for machine learning models predicting book sales, exploratory data analysis of the book publishing industry, and market analysis for authors and publishers.
- **Impact of Composition**: The dataset could lead to biased models due to potential underrepresentation of certain genres, languages, or authors. Users of the dataset should be aware of these potential biases and take steps to mitigate them in their analysis.
- **Unintended Uses**: The dataset should not be used to make decisions that impact the livelihood of individuals (e.g., authors or publishers) without proper consideration of the biases and limitations inherent in the data.

## Distribution

- **Current Distribution**: The dataset is publicly available on [data.world](https://data.world/josh-nbu) and [Kaggle](https://www.kaggle.com/datasets/thedevastator/books-sales-and-ratings).
- **License**: The dataset is subject to the terms of use found at [data.world/josh-nbu](https://data.world/josh-nbu).

## Maintenance

- **Maintainer**: The dataset is curated by **Leye Adenle**.