# Election_Analysis
## Overview of Election Audit
The purpose of this election audit is to provide deeper analysis of the [congressional](https://www.congress.gov/) election results. The information in this audit contains the voter turnout for each county, the percentage of votes from each county out of the total vote count, the county with the highest turnout and the individual candidate vote totals as well as the winner of the election. 




### Election Audit Results

* In this [congressional](https://www.congress.gov/) election were cast 369,711 total votes.
This result was acheived by using variable named **total_votes** to increment over the **election_results.csv** file within a [for loop](https://www.w3schools.com/python/python_for_loops.asp).
![image_name](https://github.com/jh2010/Election_Analysis/blob/master/images/election_total_votes.png)

#### Election total votes result
![image_name](https://github.com/jh2010/Election_Analysis/blob/master/images/total_votes.png)

---

### Breakdown of votes by County and percentage of total votes
  * Jefferson County had 38,855 votes (10.5 % of total votes)
  * Denver County had 306,055 votes (82.8% of the total votes)
  * Arapohoe County had 24,801 votes (6.7% of the total votes.

This **county vote totals** result was achieved by creating a python [dictionary](https://www.w3schools.com/python/python_dictionaries.asp) named **county_votes**.  The **county_votes** [dictionary](https://www.w3schools.com/python/python_dictionaries.asp) was populated by using a [for loop](https://www.w3schools.com/python/python_for_loops.asp) to increment through the **election_results.csv** file and using an [if statement](https://docs.python.org/3/tutorial/controlflow.html).  The [if statement](https://docs.python.org/3/tutorial/controlflow.html) added the **county name** to a list named **county_list** and then added the **county name** to the **county_votes** [dictionary](https://www.w3schools.com/python/python_dictionaries.asp) with an initial value of zero. On subsequent iterations of the [for loop](https://www.w3schools.com/python/python_for_loops.asp) the vote count for each county was incremented by on (e.g. county_votes[county_name] += 1).
![image_name](https://github.com/jh2010/Election_Analysis/blob/master/images/votes_by_county_totals.png)

The county vote percentage of total votes was achieved by using a [for loop](https://www.w3schools.com/python/python_for_loops.asp) to iterate through the **county_votes** [dictionary](https://www.w3schools.com/python/python_dictionaries.asp).  For each county, the county total votes were divided by the total votes for the election, then multiplied by 100 and stored in a variable named **county_vote_percentage**.  The **county_vote_percentage** was then printed to the terminal an then written to the text file.
![image_name](https://github.com/jh2010/Election_Analysis/blob/master/images/votes_by_county_percentage.png)

#### County vote totals and percentages result
![image_name](https://github.com/jh2010/Election_Analysis/blob/master/images/county_votes.png)

---

### County with the largest number of votes
**Denver** county had the largest voter turnout with **306,055** votes in this election.  This result was achieved by creating a variable named **county_largest_turnout_votes**, then an [if statement](https://docs.python.org/3/tutorial/controlflow.html) was used to add the county vote count to the **county_largest_turnout_votes**.  Once the [for loop](https://www.w3schools.com/python/python_for_loops.asp) finished the county with the largest voter turnout was printed to the terminal and saved to the text file.
![image_name](https://github.com/jh2010/Election_Analysis/blob/master/images/county_with_largest_turnout.png)

#### County with the largest turnout result
![image_name](https://github.com/jh2010/Election_Analysis/blob/master/images/largest_turnout_county.png)

---

### Number of votes and the percentage of the total votes each candidate received
This **candidate vote totals** result was achieved by creating a python [dictionary](https://www.w3schools.com/python/python_dictionaries.asp) named **candidates_votes**.  The **candidates_votes** dictonary was populated by using a [for loop](https://www.w3schools.com/python/python_for_loops.asp) to increment through the **election_results.csv** and using an [if statement](https://docs.python.org/3/tutorial/controlflow.html).  The [if statement](https://docs.python.org/3/tutorial/controlflow.html) added the **candidates name** to a list named **candidates_list** and then added the **candidates name** to the **candidates_votes** [dictionary](https://www.w3schools.com/python/python_dictionaries.asp) with an initial value of zero. On subsequent iterations of the [for loop](https://www.w3schools.com/python/python_for_loops.asp) the vote count for each candidate was incremented by on (e.g. county_votes[county_name] += 1).
![image_name](https://github.com/jh2010/Election_Analysis/blob/master/images/votes_by_candidate_totals.png)

The candidate vote percentage of total votes was achieved by using a [for loop](https://www.w3schools.com/python/python_for_loops.asp) to iterate through the **candidate_votes** [dictionary](https://www.w3schools.com/python/python_dictionaries.asp).  For each candidate, the candidate total votes were divided by the total votes for the election, then multiplied by 100 and stored in a variable named **candidate_vote_percentage**.  The **candidate_vote_percentage** was then printed to the terminal and then written to the text file.
![image_name](https://github.com/jh2010/Election_Analysis/blob/master/images/votes_by_candidate_percentage.png)

#### Candidates totals and percentages result
![image_name](https://github.com/jh2010/Election_Analysis/blob/master/images/candidate_vote_totals_and_percentages.png)

---

### Winning candidate, vote count, and percentage of the total votes
This result was achieved by creating variables named **winning_count**,**winning_candidate**, **winning_percentage**, and **votes** then creating an [if statement](https://docs.python.org/3/tutorial/controlflow.html).  The votes variable is generated by iteratating through the [for loop](https://www.w3schools.com/python/python_for_loops.asp) and adding the vote count from the **candidate_votes** dictionary.


The [if statement](https://docs.python.org/3/tutorial/controlflow.html) checks if the **votes** variable is greater than the **winning_votes** variable and checks if the **vote_percentage** variable is greater than the **winning_percentage**.  If this statement is true then the variable **winning_count** will be set to the value of the **votes** variable and the **winning_candidate** variable will be set to the **candidate_name** variable, then the **winning_percentage** variable is set to the **vote_percentage** variable.
![image_name](https://github.com/jh2010/Election_Analysis/blob/master/images/winning_candidate.png)

After the winning candidate details were calculated, the three variables were added to a string formated python [list](https://www.w3schools.com/python/python_lists.asp), then printed to the terminal and written to a text file.

![image_name](https://github.com/jh2010/Election_Analysis/blob/master/images/winning_candidate_terminal.png)

### Election Audit Summary
This script was created to calculate the results of the [congressional](https://www.congress.gov/) election and provide additional data to complete the election audit. This program is an easy-to-use tool for analyzing election results.  It can be modified to be used for any election.  For instance, the script could be modified to calculate the votes based on congressional district instead of county.  The change would require additional voter information that includes congressional districts.  The script is easy to maintain, it is well documented and it is not complicated.  With small modifications, it could be used for local and national elections.

