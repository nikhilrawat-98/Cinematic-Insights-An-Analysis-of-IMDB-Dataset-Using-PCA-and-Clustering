# Cinematic Insights: An Analysis of IMDB Dataset Using PCA and Clustering

This project focuses on analyzing top-rated movies from IMDB using Principal Component Analysis (PCA) and clustering methods, including K-Means and Hierarchical Clustering. The aim is to uncover patterns in movie ratings, revenues, votes, and runtime to provide insights into what makes a successful movie.

## Project Overview

- **Principal Component Analysis (PCA)**: PCA was applied to reduce the dimensionality of the dataset, simplifying the data while retaining the most important features.
- **Clustering**: K-Means and Hierarchical Clustering were used to group movies into distinct clusters based on their PCA-transformed features. The goal was to understand different movie groups based on their runtime, revenue, rating, and votes.
- **Tech Stack**: Python, Pandas, Scikit-learn, Matplotlib, Seaborn

## Dataset

The dataset consists of 50 top-rated movies on IMDB with information on their title, genre, description, director, actors, year, runtime (minutes), rating, votes, and revenue (in millions). 

### Dataset Features:
- `Title`: Movie title
- `Genre`: Movie genre
- `Description`: Brief movie description
- `Director`: Director of the movie
- `Actors`: Leading actors
- `Year`: Year of release
- `Runtime..Minutes.`: Duration of the movie in minutes
- `Rating`: IMDB rating
- `Votes`: Number of votes
- `Revenue..Millions.`: Revenue generated in millions (with some missing values imputed using the median)

## File Structure

- **`Code.ipynb`**: Jupyter notebook containing the code for the PCA and clustering analysis.
- **`Code.pdf`**: PDF version of the code for easier viewing.
- **`Report.pdf`**: Detailed report discussing the methodology, results, and conclusions from the analysis.
- **`requirements.txt`**: Python dependencies required to run the project.

## Model and Performance

### 1. Principal Component Analysis (PCA):
- **Explained Variance**: The first three principal components captured over 90% of the variance in the dataset. Key features such as `Revenue` and `Votes` contributed most to the variance, especially in the first two principal components.
- **Scree Plot and Biplot**: Visualized the explained variance and the relationship between the original features.

### 2. Clustering:
- **K-Means Clustering**:
    - Optimal number of clusters: 2 (determined using silhouette scores).
    - Silhouette Score: 0.40
    - **Cluster Profiles**:
        - **Cluster 0**: Longer movies with higher ratings, more votes, and higher revenue.
        - **Cluster 1**: Shorter movies with relatively lower ratings, fewer votes, and lower revenue.

- **Hierarchical Clustering**:
    - Distance threshold: 7 (chosen based on dendrogram analysis).
    - Silhouette Score: 0.34
    - **Cluster Profiles**: Similar to K-Means, with subtle distinctions in genres and directors across clusters.

## Usage

The Jupyter notebook demonstrates the following:
1. **Data Pre-processing**:
    - Handling missing values (imputing missing revenue values with the median).
    - Standardizing the numerical features for PCA.
2. **Principal Component Analysis**:
    - Dimensionality reduction.
    - Visualizing the explained variance using a scree plot.
    - Generating biplots to show relationships between the original features and the principal components.
3. **Clustering**:
    - Applying K-Means and Hierarchical Clustering.
    - Visualizing clusters using scatter plots and dendrograms.
    - Analyzing the cluster profiles to understand the different movie groups.

## Installation

To run the project locally:

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/Cinematic-Insights-IMDB-Analysis.git
    cd Cinematic-Insights-IMDB-Analysis
    ```

2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the Jupyter notebook:
    ```bash
    jupyter notebook
    ```

## Acknowledgements

This project was developed as part of the MSc in Business Analytics program at Bayes Business School.

## License

MIT License
