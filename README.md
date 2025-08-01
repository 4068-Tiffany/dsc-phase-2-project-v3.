### DSC PHASE 2 PROJECT ###
**Introduction**
This project explores how movie popularity from tmdb relates to movie ratings from imdb.

We analyze:
-Whether popular movies are also highly rated
-How popularity and ratings have evolved over time
-Genre trends: which genres dominate in volume, popularity, and quality

### BUSINESS UNDERSTANDING 

The movie industry generates a huge volume of content every year, but not all movies perform the same in terms of
quality and popularity. Datasets like imdb capture ratings (how much people liked a movie), while
tmdb captures popularity (attention over time).

The main objective is to answer the following key business questions:

1. **Are popular movies also highly rated?**  
   Understanding the relationship between popularity and quality helps studios and streaming platforms know if 
   marketing leads to critically good movies or just temporary attention.

2. **What trends can we observe over time?**  
   Tracking how ratings and popularity evolve over the years can help predict audience behavior, content planning, 
   and highlight shifts in audience taste.

3. **Which genres dominate the movie industry?**  
   By analyzing genres, we can find which genres:
   - Are most popular among viewers
   - Maintain consistently high ratings
   - have high quality

Ultimately, these insights help producers and marketers align investments with 
both **audience demand** and **trends**.


### DATA UNDERSTANDING

Here, i used **imdb(sqlite)**
       - movie_basics: movie_id, primary_title, start_year, genres.
       - movie_ratings: movie_id, averagerating, numvotes.
             **tmdb(excel)**
       - genre_id, original_title, popularity, release_date, vote_average, vote_count.
       
### DATA PREPARATION 
- Previewed the data in both sources to understand column names and records.
- Checked for **row counts, duplicates, missing values**, and the general structure of the datasets.
- Then merged them for combined insights ON **primary_title** and **year**
- Created a combined dataset (merged_unique) with:
**primary_title**, **start_year**, **averagerating**, **popularity**, **vote_average**, and **genres**

i chose this two because **imdb provides ratings** and **tmdb provides popularity metrics**, allowsus to analyze the relationship between them.

### Tools used
1. Python (Pandas, Matplotlib, Seaborn)
2. SQLite for joins and aggregations
3. Jupyter Notebook for exploration
4. Tableau Dashboard 
   - An interactive dashboard built from the cleaned dataset.
   - Includes charts for popularity vs ratings, trends over time, and genre insights.
5. Presentation Slides 
   - A summary of key findings and visuals from the analysis.

### Analysis and Keyfindings
1. Popularity vs Ratings
Finding: Weak positive relationship between popularity and ratings.
Insight: High popularity does not always indicate high quality.

2. Trends Over Time
-Ratings remain stable.
-Popularity shows growth in recent years due to hype marketing.

3. Genre Analysis
-Certain genres like Action, Adventure dominate in volume and popularity.
-Other genres like Documentary, Drama have high ratings despite lower popularity.

### Visualizations
1. Scatter plot: Popularity vs Ratings
2. Line plot: Trends in ratings and popularity over time
3. Combined bar & line chart: Genre frequency, average ratings, and popularity

### Conclusion
-Just because a movie is popular it doesn't mean that it is of high quality.
-Recent years show increasing hype-driven popularity
-Genre trends reveal different audience preferences 
-For deeper insights we should maybe explore **individual genre and time trends** and maybe the use of **machine learning**







