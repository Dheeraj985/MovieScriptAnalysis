### Movie Script Analysis



---

### Business Statement

Movies have unique stories that can evoke a wide range of emotions in audiences. Our project aims to analyze the sentiments and emotional tones within movie scripts, providing insights that can help writers and directors understand the potential emotional impact of their scripts on audiences. This analysis can help in refining scripts to enhance their appeal and effectiveness.

### Data Collection

We collected movie scripts from the IMSDb website, which hosts a wide range of Hollywood screenplays. The process involved:
1. **Gathering Links:** Extracting URLs of scripts using Beautiful Soup to parse the HTML `<a>` tags.
2. **Scraping Text:** Accessing the individual script pages and scraping the script text from `<tr>` and `<pre>` elements.
3. **Saving Scripts:** Saving the script texts into individual text files named after their respective movie titles.

### Preprocessing

We processed the collected scripts to extract various features and prepare the data for sentiment and emotion analysis:
1. **Scene Breakdown:** Using regex to identify and separate scenes based on keywords like "INT" and "EXT".
2. **Character Count:** Using regex patterns to count the number of characters in each script.
3. **Movie Title Extraction:** Extracting and cleaning movie titles from filenames.
4. **Runtime Calculation:** Estimating runtime based on the number of scenes, assuming an average scene duration.

### Sentiment and Emotion Analysis

We employed several tools and methods to analyze the sentiment and emotions in the scripts:
1. **Sentiment Analysis:** Using Textblob to determine the polarity of each scene, categorizing them as positive, negative, or neutral.
2. **Emotion Analysis:** Using NRCLex to identify emotions such as joy, fear, sadness, anger, etc., in each scene.
3. **Script Structure Identification:** Analyzing the narrative structure using keywords associated with different storytelling frameworks like Three-Act Structure, Hero’s Journey, etc.

### Exploratory Data Analysis (EDA)

Combining our preprocessed data with additional data such as movie ratings, budgets, and collections, we performed EDA to gain deeper insights:
1. **Correlation Analysis:** Using heatmaps to examine relationships between sentiment/emotion data and movie ratings.
2. **Box Plots:** Identifying outliers and understanding the distribution of scenes and emotions.
3. **Predictive Analysis:** Attempting to predict movie ratings using various regression models, though the correlation was found to be weak.

### Visualization

We created visualizations to better understand the data and present our findings:
1. **Emotions vs. Ratings:** Bar graphs showing the distribution of emotions in movies with different ratings.
2. **Script Structures:** Charts illustrating the prevalence of different narrative structures across movies.
3. **Scene Analysis:** Detailed visualizations of emotions present in specific scenes from movies like "Avengers: Endgame" and "American Gangster".

### Conclusion

Our analysis revealed that while sentiment and emotion analysis provide valuable insights into the emotional content of movie scripts, they are not strong predictors of movie ratings. This suggests that further research and additional features may be needed to improve predictive models. Nonetheless, understanding the emotional and structural elements of scripts can enhance storytelling and scriptwriting practices.

### Files

- **preprocess_out.csv:** Contains preprocessed data of movie scripts.
- **updated_ratings_with_budget_collections.xlsx:** Includes additional data on movie ratings, budgets, and collections.

### How to Use

1. **Data Collection:** Use the provided scripts to scrape movie scripts from the IMSDb website.
2. **Preprocessing:** Run the preprocessing steps to extract features from the collected scripts.
3. **Analysis:** Apply sentiment and emotion analysis using Textblob and NRCLex.
4. **Visualization:** Use the provided visualization scripts to explore the data and understand the findings.

### Future Work

1. **Enhance Predictive Models:** Incorporate more features and explore advanced machine learning techniques.
2. **Expand Dataset:** Collect more movie scripts and additional metadata for more robust analysis.
3. **Refine Emotion Analysis:** Improve emotion detection algorithms for more nuanced understanding.

---

This detailed summary provides a comprehensive overview of the project, from data collection and preprocessing to analysis and visualization, highlighting key findings and future directions.
