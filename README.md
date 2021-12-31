# Election_Analysis

## Challenge Overview
A Colorado Board of Elections employee has given you the following tasks to complete the election audit of a recent local congressional election.

1. Calculate the total number of votes cast.
2. Get a complete list of participating counties.
3. Calculate the voter turnout in each county.
4. Calculate each counties percentage of the the total votes cast.
5. Determine the county with the largest voter turnout.
6. Get a complete list of candidates who received votes.
7. Calculate the total number of votes each candidate received.
8. Calculate the percentage of votes each candidate won.
9. Determine the winner of the election based on popular vote.

## Resources
- Data Source: election_results.csv
- Software: Python 3.6.1, Visual Studio Code, 1.38.1

## Election Summary
The analysis of the election show that:
- There were 369,711 votes cast in the election.
- The participating counties were:
  - Jefferson
  - Denver
  - Arapahoe
- The county results were:
  - Jefferson County cast 38,855 votes which was 10.5% of the total
  - Denver County cast 306,055 votes which was 82.8% of the total
  - Arapahoe County cast 24,801 votes which was 6.7% of the total
- The highest voter turnout was in:
  - Denver County, where 82.8% of votes were cast and 306,055 votes.
- The candidates were:
  - Casper Stockham
  - Diane DeGette
  - Raymon Anthony Doanne 
- The candidate results were:
  - Charles Casper Stockham received 23.0% of the vote and 85,213 votes.
  - Diana DeGette received 73.8% of the vote and 272,892 votes.
  - Raymon Anthony Doane received 3.1% of the vote and 11,606 votes.
- The winner of the election was:
  - Diane DeGette, who received 73.8% of the vote and 272,892 votes.

## Challenge Summary
This python script can be used to quickly tabulate voting results for any election. Below are some edits that can be made to the python code to make it better suited for any election scenario.

### Edit 1
A user input prompt could be added to determine the type of election (e.g. County, City, District). That user input could be assigned to a variable (election_type). The election type variable could be used in the output. This makes the output dynamic instead of hardcoding the text.

#### Example User Input Edit 1
The user input would be put at the beginning before opening the fie.

```
# User Input to Declare Election Type
election_type = input("What kind of election is being analyzed? (County, City, District, etc.")
```

#### Example Output Edit 1
Here is a sample of the code from one of the output statements. Instead outputting the text "County" the election_type variable is used.

```
# Save the results to our text file.
with open(file_to_save, "w") as txt_file:

    # Print the final vote count (to terminal)
    election_results = (
        f"\nElection Results\n"
        f"-------------------------\n"
        f"Total Votes: {total_votes:,}\n"
        f"-------------------------\n\n"
        f"{election_type} Votes:\n")
    print(election_results, end="")

    txt_file.write(election_results)
    ```
