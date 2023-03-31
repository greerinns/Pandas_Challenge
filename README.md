# Pandas_Challenge
## File Accessing
- First it is key to access via filepath and the pandas read_csv function
## District Summary
- The number of unique schools can be determined by unique attribute of the school_name column
- The number of students is the size of the student_name column of the student dataframe
- The dataframes imported from the separate files can then be joined on the school name column to contain all the data in one frame
- Total budget is the sum of the unique budgets
- Average scores can be determined using the .mean() function in pandas on the correlating column
- the percent of students passing each subject can be found by creating new dataframes only selecting rows with a score above 70 for reading or math or both
- All the results gathered and saved under variables can be then summarized in one dataframe
## School Summary
- We can iterate through the merged data frame row by row to determine whether that row's student passes both math and reading, and then add either a 1 or a 0 to indicate passing both or not
- Then the total passing both will be the sum of that row
- We can then group by the school name to get the counts, sums, and means needed for the total students, the scores, and the both passing column
- Now we add columns to the Dataframe from the step above using the old dataframe but grouping once again by school name, this timing adding a row gate function to sum the passing students for reading and writing for each school
- Finally we can use functions between rows to calculate per student budget and the desired percentages
- Then we rename the dataframe to clean up the column titles
## School Summary Dataframe
- We create a new dataframe with specifically the columns we want for a cleaned view of the school summary
## Highest and Lowest Performing Schools
- For the top performing schools we sort the values by the % Overall Passing column, first descending and then for the lowest performing sort by descending
## Average Scores by Grade
- To determine average scores between schools by grade, we group by school_name and then grade, then average the desired score column
## Scores by School Spending
- In order to look at scores by school spending, we designate bins for the spending to be categorized by, and cut the budget per student column into 4 ranges and add the bin column to the Dataframe
- We then group by the spending ranges and use an agg function to designate column averages desired in output
## Scores by School Size
- To separate score by school size, again we designate 3 ranges for the student total column, and perform the same operation of binning and aggregating as above
## Score by School Type
- To determine scores by school type, we can groupby School type and perform the aggregate function again


