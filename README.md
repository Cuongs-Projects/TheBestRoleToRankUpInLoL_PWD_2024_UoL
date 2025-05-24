This project is a data-driven exploration into optimizing strategies for ranking up in the popular MOBA, League of Legends. It was undertaken as part of the "Programming With Data" module at the University of London (SIM). The core hypothesis investigated was: **"Aside from skills and talent, playing as a 'Bot Laner' is the best way to rank up."**

The analysis involves collecting data from various APIs, processing it using Python and relevant data science libraries, visualizing key metrics, and drawing conclusions to either support or refute the initial hypothesis, ultimately aiming to identify optimal roles, playstyles, and champion choices for competitive success.

The entire analysis is documented within the Jupyter Notebook: `[Your_LoL_Notebook_Filename.ipynb]`

- Key Objectives

1.  Identify the most successful roles among top-tier players.
   
2.  Analyze the common playstyles and in-game contributions of players in the identified optimal role(s).
   
3.  Determine the top 5 most frequently played and highest-performing champions for that role, along with their common item builds.
   
4.  Provide actionable insights for players looking to improve their ranking strategy.

- Data Sources

* Poro.gg API: Used to retrieve:
  
    * Leaderboard data for top players in the Korean server (e.g., summoner leagues, rankings).
      
    * Individual player match histories.
      
    * Champion-specific statistics for high-ranking games (build paths, win rates, matchups).
      
* Riot Games Data Dragon API: Used to retrieve:
  
    * Up-to-date lists of playable champions.
      
    * Current game version/patch information.
      
    * Static game assets like champion and item images.

- Methodology

1.  Data Acquisition: Python scripts using the `requests` library to fetch JSON data from the Poro.gg and Riot Data Dragon APIs.
   
2.  Data Processing & Cleaning:
   
    * Conversion of JSON data into `pandas` DataFrames.
      
    * Dropping irrelevant columns and filtering data (e.g., removing games shorter than 15 minutes to exclude remakes/early surrenders).
      
    * Feature engineering: Calculating metrics such as Win Rate (%), Creep Score per Minute (CS/min), and combined Kills & Assists.
      
3.  Exploratory Data Analysis (EDA) & Visualization:
   
    * Utilising `matplotlib` and `seaborn` for generating:
      
        * Pie charts (for role distribution).
          
        * Box plots (for League Points distribution by role).
          
        * Kernel Density Estimate (KDE) plots and scatter plots (for win rate vs. League Points, and pair plots for playstyle analysis).
          
    * Using `WordCloud` to visualize champion popularity.
      
4.  Insight Generation: Analyzing the visualizations and processed data to draw conclusions regarding:
   
    * Most impactful player roles.
      
    * Key performance indicators (KPIs) for successful Mid Laners.
      
    * Top champion picks and their optimal item builds.
      
5.  Ethical Considerations: Ensuring data usage aligns with API provider policies and considering potential biases.

- Key Findings & Conclusions (Summary)

 * Contrary to the initial hypothesis, **Mid Lane** (not Bot Lane) was identified as potentially the most impactful role for ranking up among top Korean players, closely followed by Jungle.
   
 * Successful Mid Laner playstyles involve proactive roaming, contributing to objectives, and maintaining a strong farm (CS/min), adapting to game state (e.g., playing safer with a high bounty).
   
 * The top 5 Mid Lane champions (as of patch [mention patch, e.g., 13.24.1] during analysis) were identified as [List top 5, e.g., Jayce, Orianna, Yone, Akali, Sylas], along with their highest win-rate core item builds.
   
 * The project provides a data-backed framework for players to reconsider their role and champion choices for climbing the competitive ladder.

- Technologies Used

* Python 3
  
* Jupyter Notebook
  
* Libraries:
  
    * `requests`
      
    * `pandas`
      
    * `numpy`
      
    * `matplotlib`
      
    * `seaborn`
      
    * `nltk` (for basic tokenisation)
      
    * `wordcloud`
      
    * `IPython.display` (for rendering HTML/Markdown in notebook)
