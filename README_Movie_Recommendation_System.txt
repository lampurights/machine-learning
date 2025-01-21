
# Movie Recommendation System

This repository contains implementations of **Collaborative Filtering** and **Content-Based Filtering** techniques to build a movie recommendation system. The project uses movie datasets to generate personalized recommendations based on user preferences and movie metadata.

---

## Features

1. **Collaborative Filtering**  
   - Predicts user preferences based on the preferences of similar users.  
   - Uses Pearson Correlation to calculate user similarity.  
   - Recommends movies based on weighted ratings from similar users.

2. **Content-Based Filtering**  
   - Recommends movies by analyzing metadata such as genres.  
   - Builds a user profile based on genre preferences and matches it with other movies.

---

## Dataset

The dataset includes:  
- **`movies.csv`**: Contains movie titles, genres, and metadata.  
- **`ratings.csv`**: Contains user ratings for movies.  

### Download and Extract the Dataset

```bash
!wget -O moviedataset.zip https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-ML0101EN-SkillsNetwork/labs/Module%205/data/moviedataset.zip
!unzip -o -j moviedataset.zip
```

---

## How to Run the Project

1. Clone this repository:  
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Install the required dependencies:  
   ```bash
   pip install pandas numpy matplotlib
   ```

3. Run the Jupyter notebooks in this order:  
   - `Collaborative_Filtering.ipynb`  
   - `Content_Based_Filtering.ipynb`

4. Modify the user inputs within the notebooks to generate personalized recommendations.

---

## Dependencies

- **Python 3.8+**  
- Libraries:  
  - `pandas`  
  - `numpy`  
  - `matplotlib`

---

## Output

The project outputs include:  
- **Collaborative Filtering**: Recommends movies based on user similarity scores and weighted ratings.  
- **Content-Based Filtering**: Provides recommendations by matching a user's genre preferences with available movies.

---

