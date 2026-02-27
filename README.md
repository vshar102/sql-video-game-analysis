# sql-video-game-analysis
An SQL-based data analysis project exploring 40 years of video game sales and Metacritic reviews. This project joins datasets to compare critic vs. user sentiments and identify the true 'golden age' of gaming history.
🎮 The Golden Age of Video Games (SQL Analysis)
📌 Project Overview
Video games are big business. The global gaming market is projected to be worth more than $300 billion by 2027. With major game publishers hugely incentivized to create the next big hit, this project seeks to answer a core question: Are games getting better, or has the golden age of video games already passed?

This project analyzes video game critic scores, user scores, and global sales data for the top 400 video games released since 1977. By leveraging SQL, I explored datasets to identify the true "golden age" of gaming—the specific release years that were loved equally by players and critics alike—while also looking into the commercial side of the industry's best sellers.

🎯 Objectives
Identify the top 10 best-selling video games of all time.
Determine the top ten release years based on average critic scores.
Find the "Golden Years" where games received universal acclaim (a score greater than 9.0) from either critics or users, and calculate the difference in their sentiment.
🛠️ Skills & Technologies Used
Language: SQL (PostgreSQL dialect)
Environment: Jupyter Notebook (DataCamp Workspace)
Concepts Applied:
Table Joins (INNER JOIN)
Data Aggregation (COUNT, AVG, ROUND)
Grouping and Filtering (GROUP BY, HAVING, WHERE)
Sorting and Limiting (ORDER BY, LIMIT)
Combining tables to perform comparative analysis and calculate differences.
🗄️ Dataset Description
The database used in this analysis consists of four main tables containing data for the top 400 video games:

game_sales: Contains the name, platform, publisher, developer, games_sold (in millions), and year of release.
reviews: Contains the name of the game along with its critic_score and user_score according to Metacritic.
users_avg_year_rating: Pre-aggregated table containing the year, num_games released, and avg_user_score for that year.
critics_avg_year_rating: Pre-aggregated table containing the year, num_games released, and avg_critic_score for that year.
📊 Key Findings & Queries
1. The Best-Selling Games of All Time
The analysis revealed that Nintendo dominates the top 10 best-selling charts, largely driven by the Wii console.

Wii Sports is the absolute best-seller with an incredible 82.9 million copies sold.
It is followed by Super Mario Bros. (NES) with 40.24M sales and Counter-Strike: Global Offensive (PC) with 40M sales.
2. Critics' Top 10 Years
By joining the game_sales and reviews tables and filtering for years with at least 4 game releases, I calculated the average critic scores per year.

1998 emerged as the undisputed favorite year for critics, with an average score of 9.32 across 10 top games.
2004 and 2002 followed closely with average scores of 9.03 and 8.99, respectively.
3. The True "Golden Years"
To truly define the golden age, I compared the average critic rating and average user rating side-by-side by joining the critics_avg_year_rating and users_avg_year_rating tables. I filtered exactly for years where either the critics or the users gave an average score above 9.0.

The Sweet Spot: 1998 had the most alignment, averaging 9.32 from critics and 9.40 from users (a tiny difference of -0.08).
The Player/Critic Divide: 1997 had the highest average user score of all time (9.50) but had a comparatively low average critic score (7.93). Conversely, critics loved 2004 (9.03), but users rated it notably lower (8.55).
