
## Methodology

### Data Preprocessing
- **Missing Values:**  
  Rows with missing `releaseYear` and `genres` are removed. For `availableCountries`, missing values are handled by filling with an empty string.
- **Feature Engineering:**  
  - `num_genres`: Count of genres per movie (splitting on commas).
  - `num_countries`: Count of available countries per movie.
- **Index Reset:**  
  The dataset index is reset to ensure consistency during data merging.

### Exploratory Data Analysis (EDA)
- **Trend Analysis:**  
  Visualization of the number of movies released over time.
- **Genre Popularity:**  
  Bar charts to show the top 10 most popular genres.
- **IMDb Ratings Distribution:**  
  Histogram and KDE plot of IMDb ratings.
- **Regional Availability:**  
  Analysis of available countries where movies are distributed (noting the data is sparse).

### Clustering
- **Objective:**  
  Group movies using K-Means clustering based on features like `imdbAverageRating`, `imdbNumVotes`, `num_genres`, and `num_countries`.
- **Process:**  
  - Standardize the features using `StandardScaler`.
  - Apply K-Means clustering with 3 clusters.
  - Merge cluster labels back into the main DataFrame for further analysis.

### Classification and Regression
- **Classification:**  
  Build a classifier (e.g., Random Forest) to predict whether a movie is "Highly Rated" based on its features.
- **Regression:**  
  Use regression models (e.g., Linear Regression) to predict IMDb ratings from the selected features.

## Results and Findings

- **Trends:**  
  A noticeable surge in movie releases was observed post-2010, highlighting Apple's growing content production.
- **Genre Popularity:**  
  The most dominant genres include Drama, Comedy, and Thriller.
- **Ratings:**  
  IMDb ratings largely fall between 6 and 8, suggesting overall favorable reception.
- **Clustering:**  
  Movies were grouped into clusters that may represent blockbusters, niche films, or lower engagement titles.
- **Regional Analysis:**  
  Limited data on regional availability, suggesting further data collection may be needed.

## Usage

1. **Clone the repository and navigate into the project directory:**
   ```bash
   git clone https://github.com/yourusername/Data-analysis-on-Apple-tv.git
   cd apple-tv-plus-analysis
