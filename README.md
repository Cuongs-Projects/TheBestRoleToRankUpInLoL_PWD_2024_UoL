# Project: 'Bot Laner' - The Optimal Role to Rank Up in League of Legends?
## Year 2 Semester 2 - Programming With Data (SIM UoL)

This repository contains the project for the "Programming with Data" module. The project investigates the hypothesis: **"Aside from skills and talents, the playing as ‘Bot Laner’ is the best way to rank up in League of Legends.”** 

It utilizes Python with libraries such as Pandas, Matplotlib, Seaborn, and NLTK to fetch, process, analyze, and visualize data from League of Legends APIs (Poro.gg and Riot's Data Dragon) to determine optimal strategies for ranking up, focusing on role selection, playstyle, and champion/item choices.

You can view the entire at the Jupyter Notebook 

"Aside from skills and talents, 'Bot Laner' is the best role to rank up in League of Legends.ipynb"

- Code Origin and Development Approach:

The development of this project followed a standard data analysis workflow:

  *Core Analytical Flow & Logic --> API Interaction & Library Usage --> Dataset Understanding --> Module Learning

- Project Structure & Key Analytical Stages:

The project is structured into several analytical stages, detailed within the Jupyter Notebook:

1. An Introduction to the Research Space:
   
    *Objective: Clearly define the project's hypothesis and goals.
   
    *Datasets: Identify the primary data sources: Poro.gg API (leaderboards, match data, champion stats) and Riot Games Data Dragon API (game versions, champion lists, item images).
   
    *Methodology: Outline the use of Jupyter Notebook for data processing and analysis.
   
    *Context on League of Legends: Provide essential background information on League of Legends gameplay, roles, and map structure.
   
    *Implementation: Primarily textual descriptions, API endpoint listing.

3. Project Background:
   
    *Motivation: Explain the personal interest and rationale behind the research question.
   
    *Novelty: Discuss the existing landscape of LoL guides and the project's aim to provide a data-driven perspective.
   
    *Scope: Define the specific areas of investigation: role success, common playstyles, and champion/item choices.
   
    *Pipeline: Detail the analytical data processing steps (retrieve, process, clean, save, visualize, analyze).

5. Retrieving Necessary Starting Data:
   
    *Latest LoL Version: Fetch the current game version using the Data Dragon API (`requests`).
   
    *Playable Champions List: Retrieve and process champion data from Data Dragon, saving it to a CSV (`requests`, `pandas`).
   
    *Top 500 KR Players: Acquire leaderboard data for the top 500 players on the Korean server from the Poro.gg API, process, and save to CSV (`requests`, `pandas`).
   
    *Implementation: Python functions for API calls, DataFrame creation, data cleaning, CSV I/O.

7. Data Relevance and Justification:
   
    *Data Origin & Acquisition: Detail the sources (Poro.gg, Data Dragon) and API inspection techniques.
   
    * Appropriateness: Justify why these data sources (especially the Korean server data) are suitable for the research.
    * 
    *Data Format: Confirm the suitability of JSON (from APIs) and CSV (for storage/re-use) for analysis with Pandas.

    *Alternative Datasets: Consider and evaluate other potential datasets (e.g., professional match data, OP.gg) and their strengths/weaknesses for this project's scope.

9. Ethics of Use of Data:
    
    *Source Transparency: Reiterate that data comes from publicly accessible APIs.
   
    *Usage Considerations: Discuss Riot Games' API policy and ensure compliance.
   
    *Implications & Bias: Address potential implications of using the data and consider any potential biases in the datasets (concluding they are objective game records).

11. Hypothesis Testing: Is "Bot Laner" the Best Role to Rank Up?
    
    *Preferred Roles Analysis: Calculate and visualize the distribution of preferred roles among the top 500 players (`pandas`, `matplotlib` pie chart).
    
    *League Points (LP) by Role: Compare LP distributions across different roles using boxplots (`pandas`, `seaborn`).
    
    *Win Rate vs. LP by Role: Analyze the relationship between win rate and LP, segmented by role, using joint KDE plots and scatter plots with trendlines (`pandas`, `seaborn`, `numpy`, `matplotlib`).
    
    *Conclusion: Summarize findings and revise the initial hypothesis, identifying Mid Lane as potentially more optimal.


13. In-Depth Analysis: Playstyle of Mid Laners
    
    *Mid Laner Profile Retrieval: Fetch match history for Mid Laners from the top 500 list using the Poro.gg API (`requests`, `pandas`).
    
    *Performance Data Processing: Normalize and clean player performance data from match details. Implement outlier removal for games ending too early (e.g., remakes/early surrenders). Calculate metrics like CS per Minute (`pandas`).
    
    *Contribution Comparison: Use pair plots to visualize relationships between various performance metrics (e.g., damage to objectives, CS per minute, vision score, kills/assists) and game outcomes (win/loss) (`seaborn`, `pandas`).
    
    *Passivity Analysis: Investigate if a more passive playstyle is beneficial by analyzing metrics like deaths, bounty level, and CS per minute in relation to game outcomes (`seaborn`, `pandas`).
    
    *Summary: Derive actionable playstyle recommendations for Mid Laners.
    
    *Implementation:, complex DataFrame manipulation, advanced statistical visualizations.

15. Champion and Item Recommendations for Mid Laners:
    
    *Top 5 Most Played Champions: Identify the most frequently played Mid Lane champions among top players using frequency distributions and visualize with a word cloud (`pandas`, `nltk.FreqDist`, `wordcloud`).
    
    *Core Item Builds: Fetch champion-specific statistics (including item builds) from Poro.gg API for the identified top champions. Filter for the highest win-rate core item builds (`requests`, `pandas`).
    
    *Data Combination: Merge champion information with their optimal item builds.
    
    *Visual Summary: Present the top 5 Mid Lane champions with their recommended core items and champion/item images (fetched via Data Dragon API) using HTML within the notebook.
    
    *Implementation: Text processing, API calls for detailed stats, data merging, dynamic HTML generation for presentation.

17. Conclusion:
    
    *Summary of key findings of the entire project, shift from the initial hypothesis and highlighting the data-driven insights gained regarding optimal role, playstyle, and champion/item choices for ranking up in League of Legends.

- Technologies Used:
  
*Python 3

*Jupyter Notebook

*Pandas

*NumPy

*Matplotlib

*Seaborn

*Requests: For making HTTP requests to APIs.

*NLTK (Natural Language Toolkit): Specifically `FreqDist` for champion frequency and `word_tokenize` (though `ast.literal_eval` might be more robust for list-like strings).

*WordCloud: For generating word cloud visualisations.

*IPython.display: For rendering HTML and Markdown within the Jupyter Notebook.

