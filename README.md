# Election_Analysis

## Overview of Election Audit
A Colorado Board of Elections employee has asked that an audit be performed of a recent local congressional election to include the following tasks. 

1. Calculate the total votes cast
2. Get a complete list of candidates who received votes. 
3. Calculate the total number of votes each candidate received. 
4. Calculate the percentage of votes each candidate won. 
5. Determine the winner of the election based on popular vote. 
7. The voter turnout for each county
8. The percentage of votes from each county out of the total count
9. The county with the highest turnout


## Resources
- Data Source: election_results.csv
- Software: Python 3.7.6, Visual Studio Code 1.54

## Election-Audit Results
The analysis of the election shows:
- There were 369,711 votes cast in the election.
- The candidates were:
   -Charles Casper Stockham
   -Diana Degette
   -Ramon Anthony Doane
- The candidate results were:
   - Charles Casper Stockham received 23% of the vote and 85,213 votes.
   - Diana Degette received 73.8% of the vote and 272,892 votes.
   - Ramon Anthony Doane received 3.1% of the vote and 11,606 votes.
-The winner of the election was:
   - Diana Degette who received 73.8% of the vote and 272,892 votes.
- The counties casting votes in this election were:
   - Jefferson
   - Denver
   - Arapahoe
- The voter turnout for each county were:
   - Jefferson: 38,855
   - Denver: 306,055
   - Arapahoe: 24,801
- The percentage of total votes from each county were:
   - Jefferson: 10.5%
   - Denver: 82.8%
   - Arapahoe: 6.7%
- The county with the highest turnout was:
   - Denver

## Election-Audit Summary
Writing code of this type, performing the tasks requested of the Colorado Board of Elections, is time consuming.  Requiring personnel to re-create this code may lead to errors.  Knowing that this type of audit analysis could be required in the future, the code was written so that it could be applied to future, or past, election data files with minimal modification.  Using the same code maintains consistency through the analysis of data, as long as the source data shares the same formatting as the data with which the code was written to process.  

There is one change that would be required to utilize this code with other data sources:
1.  Updating the source data name in the script.  The following script would need to be changed so that the correct data file is being utilized for the analysis. 

                Line 9  file_to_load = os.path.join(".", "Resources", "election_results.csv")

    This line of script identifies the folder and file name that is being used for the source data of the analysis.  "Resources" is the parent folder that holds the file         "election_results.csv".  
    
Other changes that could be made would be for reporting purposes:
1.  If any task is determined to be non-essential for the analysis, adding a "#" to the begging of the line will force Python to not run that code.  Focus on adding this only     to the "print" functions to minimize any calculation issues.  This means that all the calculations and scripting are being performed, and data will be available, but         will not be printed on the report unless the "#" is removed.  An example is line 105 where the county results are printed:
    
                print(county_results)
    
    To prevent the script from printing these results, add "#" to the beginning of the line:
    
                # print(county_results)

2.  The output text file may need to be updated depending on location and name required.  Currently the file is identified on line 11 as: 
            
                file_to_save = os.path.join("analysis", "election_analysis.txt")
    
    Just as Line 9 above showed the folder and file name, so does line 11, but for the output file and folder that the file resides.  These would need to be changed if           needed. 
