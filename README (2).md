# Project: Project: Data Modeling with Cassandra



------------------------------------------
### Purpose Overview
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analysis team is particularly interested in understanding what songs users are listening to. Currently, there is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app.

--------------------------------------------
### Project Structure 

+ `Project_1B_ Project_Template.ipynb` - this python notebook proccess all csv files in event_data folder to create event_datafile_new.csv then for a given query we create here table (for optimisation) and insert data on it 

--------------------------------------------
### query Exemple
The following diagram show the star schema used in this project


####  Query 1
1. Get the artist, song title and song's length in the music app history that was heard during sessionId = 338, and itemInSession = 4 
`SELECT artist, song, length FROM song_history_by_session WHERE sessionId = 338 AND itemInSession = 4`

####  Query 2
2. #### GET artist_name,song_name(sorted by itemInSession) and user for userid = 10, sessionid = 182 : 
`SELECT artist_name, song_name, itemInSession, user_first_name, user_last_name FROM song_history_by_userID WHERE userid = 10 AND sessionid = 182`

####  Query 3
3. Get all users who listened to the song 'All Hands Against His Own' :
`SELECT user_first_name, user_last_name FROM song_history_by_songName WHERE song_name = 'All Hands Against His Own`

