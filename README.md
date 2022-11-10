# Election Results
## Overview
We were provided voting data from the Colorado board of elections, with details of a U.S. congressional election. The data included the selected candidate and the county in which the voter was representing. We were asked to summarize the results of the election at the candidate, county and overall election levels.

## Results
  - How many votes were cast in this congressional election?
  ```
  Total Votes: 369,711
  ```
  - Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct.
   ```
  County Votes:
  Jefferson: 10.5% (38,855)
  Denver: 82.8% (306,055)
  Arapahoe: 6.7% (24,801)
  ```
  - Which county had the largest number of votes?
  ```
  Largest County Turnout: Denver
  ```
  - Provide a breakdown of the number of votes and the percentage of the total votes each candidate received.
  ```
  Charles Casper Stockham: 23.0% (85,213)
  Diana DeGette: 73.8% (272,892)
  Raymon Anthony Doane: 3.1% (11,606)
  ```
  - Which candidate won the election, what was their vote count, and what was their percentage of the total votes?
  ```
  Winner: Diana DeGette
  Winning Vote Count: 272,892
  Winning Percentage: 73.8%
  ```
## Summary
The exact script can be reused again for another similar election without any coding changes. The use of the "os.path.join" logic will allow a new file to be referenced as long as the folder hierarcy of the file and the script remain the same. The voting data file (csv format) should be in a folder called "Resources" which lives in the same folder as the script. In addition, a blank folder called "analysis" should live at this level to allow for the output.

As example, I copied the original analysis, keeping the script, gitignore file, and the two folders (Resources/analysis). I then added 100 extra votes to the original data to mock up new results, and saved it in the Resources folder. When I rerun the script, I am provided updated outcomes.
  ```
  County Votes:
  Jefferson: 10.5% (38,855)
  Denver: 82.8% (306,055)
  Arapahoe: 6.7% (24,801)
  New County: 0.0% (100)
  -------------------------
  Largest County Turnout: Denver
  -------------------------
  Charles Casper Stockham: 23.0% (85,213)
  Diana DeGette: 73.8% (272,892)
  Raymon Anthony Doane: 3.1% (11,606)
  New Candidate: 0.0% (100)
  ```
 This election's winner is the candidate with the most votes, regardless if they had the majority of the total votes. If the election rules changed to require that the candidate receive the majority of votes (more than 50%), the coding could be updated easily to respect this new rule. If no candidate received the majority, no name will appear in the results.

```Python
 # Determine winning vote count, winning percentage, and candidate.
        if (vote_percentage > 50):
            winning_count = votes
            winning_candidate = candidate_name
            winning_percentage = vote_percentage
```
