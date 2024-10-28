## Submission 

Add the required code in the respective files action.ipynb and medals.ipynb. Commit your code and requested .csv files.md file to the repository.  For the Action problems, enter your solutions in the solutions.txt file.

Be sure all of your column names are created as specified in the instructions (case sensitive). This will allow for easy comparisons for grading.

## #1
In the action.ipynb file, use `requests`, `BeautifulSoup`, and `pandas`, create a DataFrame of the
[140 Essential Action Movies](httpseditorial.rottentomatoes.comguide140-essential-action-movies-to-watch-now)
as selected by Rotten Tomatoes. 

Your DataFrame should have 140 rows and 5 columns

 Title  Year  Score  Rank  Category 
 ----------------------------------------

where 
- Title is the movie title,  
- Year is the year the movie came out,  
- Score is the tomato meter score,  
- Rank is the assigned ranking from 1 to 140 (ranked by score, ties are okay)  
- Category is the rating category used by Rotten Tomatoes and should be Certified Fresh, Fresh, or Rotten

Title and Category should be type object.  Year, Score, and Rank should be type int.
Sort the DataFrame by Score and reset the indexing with df.reset_index(drop = True)

### Answer the following

(a) Report the mean score of the list.  

(b) What is the correlation coefficient between Score and Rank.   

(c) What is the mean Rank of each Category.    

(d) Create a column, Decade, that represents the decade (e.g., 1960, 1990). This should have an integer dtype.

(e) Get the count of movies per decade and the average Score per decade.  

(f) Save your dataframe as a .csv file called action.csv. Use the index = False arguement

---

## #2

In medals.ipynb, you will be using `pd.read_html` and the following Wikipedia page to clean up a table of Olympic Medals

 [httpsen.wikipedia.orgwikiAll-time_Olympic_Games_medal_table](httpsen.wikipedia.orgwikiAll-time_Olympic_Games_medal_table)

Follow the below instruction to provide a clean table of the medals data

(a) Read in the main table from the url under the section List of NOCs with medals (sortable & unranked)  

(b) The table will come with two headings (one is pulling the image data). Drop the messy heading using Pandas droplevel function.  

(c) Rename the respective columns to 'Team', 'Summer Olympics', 'Summer Gold', 'Summer Silver', 'Summer Bronze', 'Summer Total', 'Winter Olympics', 'Winter Gold', 'Winter Silver', 'Winter Bonze', 'Winter Total',    'Combined Olympics', 'Combined Gold', 'Combined Silver', 'Combined Bronze', 'Combined Total' 
                  
(d) Use regular expressions to extract the three-letter abbrebiations from the Team column. Create a new column from these abbreviations called IOC. Put this column in the second column position (immediately following the team name). Do not include the parentheses in this column, just the abbreviation.  

(e) Clean the Team column values (e.g., remove all abreviations, links, etc.) Only the team name should be left.  

(f) Remove the Totals row.  

(g) Sort the dataframe by 'Summer Gold', then 'Winter Gold' in descending order and reset the indexing with df.reset_index(drop = True)

(h) Use the pandas to_markdown function and save the output as a .md file, called medals.md.

(i) Save your dataframe as a .csv file called medals.csv. Use the index = False arguement
