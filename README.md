# 🎬 Movies EDA (Pandas & Seaborn)

## 📌 Overview
This project performs Exploratory Data Analysis (EDA) on a movie dataset using Python, Pandas, and Seaborn.
The main focus is on data visualization to understand movie popularity, ratings, and genre trends across different languages and years.

---

## 📊 Dataset
The dataset contains information about movies, including:
* **Title & Release Date** (Year extracted for time-based analysis)
* **Genre** (Multi-genre entries split for detailed analysis)
* **Popularity Score** (Numeric score reflecting audience engagement)
* **Vote Count & Vote Average** (Rating data from audience votes)
* **Original Language** (Language the movie was produced in)

Each row represents one movie.

---

## 🎯 Objectives
* Explore the most popular genres and movies
* Analyze how original language affects popularity
* Investigate the relationship between vote count and rating quality
* Track genre trends over time
* Identify the highest rated genres and compare them to the most popular ones

---

## 🧹 Data Cleaning
* Extracted **Year** from `Release_Date` using `pd.to_datetime()`
* Dropped irrelevant columns: `Overview` and `Poster_Url`
* Removed a **corrupted row** where `Original_Language` contained a URL
* Removed **duplicate rows**
* Converted `Vote_Average` and `Vote_Count` to numeric using `pd.to_numeric(..., errors='coerce')`
* Split and exploded the `Genre` column to handle multi-genre entries

---

## 🧪 Analysis Steps

### 1️⃣ Most Popular Genres
* Exploded multi-genre entries and summed popularity scores per genre
* Visualized the top 10 genres using a horizontal bar plot
* Helps understand what genres audiences engage with most

### 2️⃣ Most Popular Movies
* Sorted movies by popularity score and visualized the top 10
* Identified standout blockbusters vs the rest of the dataset

### 3️⃣ Genre of the Most Popular Movie
* Queried the dataset for Spider-Man: No Way Home's genre
* Connected the most popular movie to the top-performing genres

### 4️⃣ Language vs Popularity
* Summed popularity scores per original language
* Visualized the top 10 languages to show English dominance
* Analyzed how language contributes to the success of top movies

### 5️⃣ Film Production Over Time
* Extracted year from release dates and counted films per year
* Used a line plot to show production trends from 2000 to 2022
* Highlighted the COVID-19 dip in 2020 and the 2021 rebound

### 6️⃣ Highest Rated Genres
* Calculated average `Vote_Average` per genre after exploding genres
* Compared highest rated genres against most popular genres
* Revealed the gap between critical quality and audience popularity

### 7️⃣ Vote Count vs Vote Average
* Scatter plot of `Vote_Count` vs `Vote_Average`
* Analyzed the reliability of ratings based on number of votes
* Identified the funnel effect — fewer votes leads to more extreme scores

### 8️⃣ Genre Trends Over Time
* Tracked the top 4 genres by movie count from 2000 to 2022
* Used a multi-line plot with one line per genre
* Showed how genre production shifted over the years

---

## 📈 Tools & Libraries
* Python
* Pandas
* Seaborn
* Matplotlib

---

## ✅ Key Insights
* **Action** is the most popular genre but accounts for only ~12% of total popularity — interest is spread across genres
* **Spider-Man: No Way Home** is the most popular movie, scoring 121x above the English language average
* **English** is the dominant language, representing ~76% of all movies in the dataset
* **History & War** are the highest rated genres, despite being far less popular than Action
* **2021** had the highest film production, likely a post-COVID rebound effect
* **Vote count is a trust signal** — ratings stabilize between 7–9 only when vote count is high
* **Drama** grew the fastest over time, peaking at 265 movies in 2021

---
ll pandas seaborn matplotlib
```
3. Place `mymoviedb.csv` in the project directory
4. Open and run `Movies_EDA-Visuals.ipynb` in Jupyter Notebook
