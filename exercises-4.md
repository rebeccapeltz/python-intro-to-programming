# Using API's

API stands for Application Programming Interface.  It is a way for developers to get data from the internet.

We use [Postman](https://www.getpostman.com/downloads/) to analyze the data in order to see how to include it in our app.    


## The Numbers API
Here we can find interesting facts about Numbers
```Python
import requests, json


data = requests.get("http://numbersapi.com/19?json")
dict = json.loads(data.content)
print(dict)

print ("The type of the object  returned from the internet is", type(data))
print ("The type of the content returned from the internet is", type(data.content))
print ("The type of the data that the json.loads command creates is ", type(dict))

print("The interesting thing about 19 is: ", dict["text"])
```

## Cat facts
(https://catfact.ninja)[https://catfact.ninja]  

```Python
import requests, json

data = requests.get("https://catfact.ninja/breeds?limit=5")
dict = json.loads(data.content)
print(dict["data"])

for cat in dict["data"]:
  for property in cat:
    print(property,":",cat[property])
  print("------------")
```

## NBA Facts
```Python

import requests, json

data = requests.get("https://data.nba.net/")
dict = json.loads(data.content)
team_data = dict["sports_content"]["teams"]["team"]
# print (team_data)
for team in team_data:
  if (team["is_nba_team"]):
    print(team["team_abbrev"],team["team_nickname"], team["conference"], team["division_id"])
 
```
## Pokemon
```Python
import requests, json

data = requests.get("https://pokeapi.co/api/v2/pokemon")
dict = json.loads(data.content)

results = dict["results"]
for result in results:
  print(result["name"])
```


