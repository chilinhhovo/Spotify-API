# Spotify API

 This was a homework from week 5 from Jonathan Soma's class. 
 
The mission
On Spotify, there is a playlist called Fall in a 90s Suburb while researching the band SEAGULL SCREAMING KISS HER KISS HER. The playlist was pretty good, but since since SSKHKH only has like 1,500 listeners each month Soma was curious about the most/least popular songs on the playlist.

The questions
What are the ten most popular songs on the playlist?
What percentage of them have a popularity of zero? Print them out, sorted by the band name.
Is popularity relative to the artist, the album, all songs on Spotify, or something else?
My suggested approach

The suggested steps:

Getting the playlist and print out its name and description.
Print out the name and popularity of each song
Print out the name, popularity, and artists of each track on the playlist. Or, if you'd like a shortcut, just pick the first artist.
Instead of printing, use these to create a new dictionary each time you look at a track. Print out this dictionary. You should be printing out 476 dictionaries!
Printing isn't helpful! Instead, after you create the dictionary append it to a list called all_tracks
When you're done, all_tracks should have 476 items in it
Sort the list by popularity, take the top ten
Filter the list by popularity, selecting only the ones with a popularity of 0
Tips
Spotipy documentation: https://spotipy.readthedocs.io/

Spotify Web API documentation: https://developer.spotify.com/documentation/web-api/

Tips: 
Do this in many, many cells, not all in one!
You definitely want to look at the Spotipy examples to find some good code to base your answer off of. There are a handful that talk about playlists – it might be helpful to read and compare a few of them!
Getting the playlist name/description is a different endpoint than getting the actual songs on the playlist.
Are you printing out the same number of tracks as are in the actual playlist? Take note and be careful! It should be ~476.
If you're getting the id of playlist songs but not seeing song names, look for fields='items.track.id,total in your code. It's only pulling the track's id! Change it to items.track,total and it will return more information about each track
all_tracks = [] should be the first line in your cell. That makes sure it always resets to being empty before you start adding tracks to it.
Be sure the first and last items in all_tracks are different – maybe you're accidentally adding the same item each time!
Normally we sort lists of numbers, which is easy. Sorting a list of dictionaries can be done easily with key=. Look it up!
Pick the most popular 10 songs using list comprehensions
Filtering is best done with a list comprehension.
You can sort by things that aren't numbers!
