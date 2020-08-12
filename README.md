# Election_Analysis
## Overview of Election Audit
The purpose of this election audit is to provide deeper analysis of the election results. The information in this audit contains the voter turnout for each county, the percentage of votes from each county out of the total vote count, the county with the highest turnout and the individual candidate vote totals. 

### Election Audit Results

* In this congressional electecion were cast 369,711 total votes.
This result was acheived by using variable named **total_votes** to increment over the **election_results.csv** file within a [for loop](https://www.w3schools.com/python/python_for_loops.asp).
![image_name](https://github.com/jh2010/Election_Analysis/blob/master/images/election_total_votes.png)


* Breakdown of votes by County and percentage of total votes
  * Jefferson County had 38,855 votes (10.5 % of total votes)
  * Denver County had 306,055 votes (82.8% of the total votes)
  * Arapohoe County had 24,801 votes (6.7% of the total votes.

This county vote totals result was achieved by creating a python dictionary named **county_votes**.  The **county_votes** dictonary was populated by using a [for loop](https://www.w3schools.com/python/python_for_loops.asp) to increment through the **election_results.csv** and using an [if statement](https://docs.python.org/3/tutorial/controlflow.html).  The [if statement](https://docs.python.org/3/tutorial/controlflow.html) added the **county name** to a list named **county_list** and then added the **county name** to the **county_votes** dictionary with an initial value of zero. On subsiquent iterations of the [for loop](https://www.w3schools.com/python/python_for_loops.asp) the vote count for each county was incremented by on (e.g. county_votes[county_name] += 1).
![image_name](https://github.com/jh2010/Election_Analysis/blob/master/images/votes_by_county_totals.png)

The county vote percentage of total votes was achieved by using a [for loop](https://www.w3schools.com/python/python_for_loops.asp) to iterate through the **county_votes** dictionary.  For each county the county total votes was divided by the total votes for the election, then multipied by 100 and stored in a variable named **county_vote_percentage**.  The **county_vote_percentage** was then printed to the screen an then written to the text file.
![image_name](https://github.com/jh2010/Election_Analysis/blob/master/images/votes_by_county_percentage.png)


* County with the largest number of votes
**Denver** county had the largest voter turnout with **306,055** votes in this election.  This result was achieved by creating a variable named **county_largest_turnout_votes**, then an [if statement](https://docs.python.org/3/tutorial/controlflow.html) was used to add the county vote count to the **county_largest_turnout_votes**.  Once the for loop finished the county with the largest voter turnout was printed to the screen and saved to the text file.
![image_name](https://github.com/jh2010/Election_Analysis/blob/master/images/county_with_largest_turnout.png)

* Number of votes and the percentage of the total votes each candidate received


* Winning candidate, vote count, and percentage of the total votes





### Election Audit Summary
