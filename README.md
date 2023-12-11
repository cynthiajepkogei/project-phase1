# project-phase1Microsoft Studio - Unlocking the Tri-fecta of Triumph
By Cynthia Jepkogei

Overview of Microsoft's Potential Entry into Original Video Content
This project aims to provide valuable insights for Microsoft Studios' strategic decision-making process to enter the original video content market. The analysis focuses on three key areas where Microsoft can capitalize on its strengths:

1. Business Partnerships
Partnering with established studios or streaming platforms can offer immediate access to expertise, resources, and distribution channels. This strategic move mitigates the risks associated with entering a saturated market, addressing Microsoft's lack of experience in content production and streaming.

2. Content Selection
Leveraging descriptive statistics and exploratory data analysis, the project identifies film genres and types that currently perform well at the box office. This data-driven approach guides Microsoft Studios in selecting commercially viable content for production.

3. Personnel/Hiring
Building a strong team with experienced professionals in film production, content creation, and streaming platform management is crucial. Active recruitment of industry veterans and subject-matter experts addresses Microsoft's current lack of domain-specific knowledge.

Addressing the Business Problem
Saturated Market:

Partnering with established players and data-driven content selection can help Microsoft navigate the crowded market effectively.
Lack of Experience:

Strategic partnerships bridge the experience gap, providing valuable industry insights.
Lack of Subject Matter Experts:

Active recruitment of industry professionals addresses the shortage of subject-matter experts.
Data Sources and Integration
The project utilizes data from five reputable online databases:

IMDb and Box Office Mojo by IMDb
Rotten Tomatoes
The Movie Database
The Numbers
Data integration was achieved through unique identifiers for movies and crew, alongside movie name matching, ensuring accurate and reliable information.

python
# Sample code for reading data into DataFrames
import pandas as pd
import sqlite3

# Read CSV files
bom_movie_gross = pd.read_csv('bom.movie_gross.csv.gz')
rt_movie_info = pd.read_csv('rt.movie_info.tsv.gz', sep='\t', compression='gzip')

# Connect to SQLite database
conn = sqlite3.connect('im.db/im.db')
imdb = pd.read_sql_query("SELECT * FROM movie_basics;", conn)
Data Cleaning
The cleaning process involves handling duplicates, missing values, and converting numeric columns where necessary.

python
# Sample code for data cleaning
bom_movie_gross = bom_movie_gross.drop_duplicates().dropna()
rt_movie_info = rt_movie_info.dropna().drop_duplicates()

Exploratory Data Analysis
Exploration of IMDb and TMDb data provides insights into genres, directors, and writers. Visualizations help identify trends and preferences in the film industry.
python
# Sample code for exploratory data analysis
# Convert 'box_office' column to numeric (if not already)
rt_movie_info_cleaned['box_office'] = rt_movie_info_cleaned['box_office'].replace('[\$,]', '', regex=True).astype(float)
# Sort the DataFrame by 'box_office' in descending order
rt_movie_info_sorted = rt_movie_info_cleaned.sort_values(by='box_office', ascending=False)
# Print the result
print(rt_movie_info_sorted[['writer', 'box_office']])
# Visualize top studios, genres, directors, and writers

Evaluation of Microsoft Studios' Entry
Insights from the analysis lead to actionable recommendations for Microsoft Studios:
1. Studios:
Partner with IFC Films and Sony Pictures for distribution channels and expertise.
2. Genres:
Focus on producing dramas, documentaries, and comedies for critical acclaim.
Directors:
Collaborate with directors who demonstrate both financial and critical success.
3. Writers:
Consider hiring writers like Sebastien Lifshitz, Jamie Buckner, and Joe Camp in recommended genres.

Conclusions
Entering the competitive video content market requires strategic planning. Leveraging partnerships, selecting the right content, and assembling a talented team position Microsoft Studios for success.

Actionable Recommendations
1. Strategic Partnerships:
Partner with IFC Films and Sony Pictures for immediate access to expertise and distribution channels.
Content Strategy:

2. Focus on producing dramas, documentaries, and comedies based on genre performance data.
Talent Acquisition:

3. Recruit experienced directors and writers, considering individuals with a proven track record in recommended genres.
This comprehensive analysis equips Microsoft Studios with actionable insights for a successful entry into the original video content market.
