# CSTopics1HW3
University of Iowa CS:3980:001 HW3

The goal of this assignment was to get familiar with Mongodb databases and mongosh. The movies database was loaded as a sample database from Mongodb. 

A Mongodb atlas account was made and Mongodb Compass was downloaded. A cluster was made and the movies database was loaded as a sample database. The cluster was connected with the Mongodb Compass app by copying and pasting the connection string into Mongodb Compass. Then, the sample loaded databases were accessesed in mongosh by the following command:
```powershell
use sample_mflix
```
Then, commands were used to find the movies described in (1) and (2) below.

(1) To find all the movies released in 1983 with a runtime longer than 200 minutes the following command was run in mongosh:
```powershell
db.movies.find({ 'runtime': { $gt: 200 }, 'year':1983 }, {title:1, runtime:1, year:1, '_id': false})
```

The code and results are shown in the image below.

<img width="600" alt="Screenshot 2024-03-26 at 1 41 03 PM" src="https://github.com/samanthapoth/CSTopics1HW3/assets/90707077/c8d47d78-bd6f-4630-b35e-ea271c573903">



(2) To find all the movies released after 2014 with an imdb rating greater than 9, the following command was run in mongosh:
```powershell
db.movies.find({ 'year': { $gt: 2014 }, 'imdb.rating': { $gt: 9 } }, {title:1, imdb: {rating:1}, year:1, '_id': false})
```

The code and results are shown in the image below.

<img width="700" alt="Screenshot 2024-03-26 at 1 24 46 PM" src="https://github.com/samanthapoth/CSTopics1HW3/assets/90707077/131c49bb-32ee-47f2-a8b2-3b1164d2f434">
