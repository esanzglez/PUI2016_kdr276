# PUI 2016 HW2 - Kelsey Reid

## Assignment One - Tracking Each Vehicle For a Line:

For this assignment I created a python script file that takes 2 arguments to report MTA API data of the number and location of buses of a given bus line. The first argument being the MTA key assigned to the specific user and the second being the desired bus line. 

Once I obtained my key I requested data from the BusTime API server and copied the data into a JSON formatter to better understand the hierarchy of nested dictionaries and lists. Once I could understand the specific keys to the information I wanted to report, I was able to make a print statement to print the information for the chosen bus line. I then created a for loop with a counter to print a total of buses active on the chosen line and a for loop to report the longitude and latitude of each active bus. Once I was confident the code ran properly I replaced my key and bus line information in the url with variables to represent the arguments to be passed from the command line.
Written and tested in Python 2.7 

Homework help group includes Will Xia, Marc Toneatto, Matt Slone, Ozgur Akkas - assisted MS in providing dictionary/list structure from API data to pull the longitude and latitude values, shared over group email

## Assignment Two - Next Stop information

For this assignment I used the code I created for assignment one as a base to edit and build upon. I used a for loop to iterate over the values desired for the .csv file. Code used to generate the .csv file was found at [http://michelleminkoff.com/2011/02/01/making-the-structured-usable-transform-json-into-a-csv/](http://michelleminkoff.com/2011/02/01/making-the-structured-usable-transform-json-into-a-csv/) which I accessed on Sept 19th, 2016 and shared with my homework team via email. I replaced my dictionary keys with those in the example I found and ran the output to a test file on multiple bus lines.
Confirmed output to file was corrected and added if/else statements for 'Stop Name' and 'Stop Status' categories so that if the entry was blank 'N/A' would be the output added to the information fields
Written and tested in Python 2.7 

## Assignment Three - Read CSV File With Pandas
Chose to use DSNY Refuse and Recycling Disposal Netorks data .csv from the datahub site. Confirmed os.getenf('DFDATA') pointed to correct data facility location
Difficulty opening the .csv file from this point with pandas, the DFDATA + datset location (/kzmz-ivhb) did not work so via Juypter Hub I traversed through the file location to find the additional file location information (/1414245874/kzmz-ivhb). Shared with my group my method to find the full path information
Used the .head() command to pull only the first 5 lines of the file and the .drop command to remove the all column headers except for two numerical - the longitude and latitude of each facility location.
Plotted the cooridnate information using plot.scatter 
