## What Google Learned About Teams

Project Aristotle’s researchers began by reviewing a half-century of academic studies looking at how teams worked. Were the best teams made up of people with similar interests? Or did it matter more whether everyone was motivated by the same kinds of rewards? Based on those studies, the researchers scrutinized the composition of groups inside Google: How often did teammates socialize outside the office? Did they have the same hobbies? Were their educational backgrounds similar? Was it better for all teammates to be outgoing or for all of them to be shy? They drew diagrams showing which teams had overlapping memberships and which groups had exceeded their departments’ goals. They studied how long teams stuck together and if gender balance seemed to have an impact on a team’s success.

## Hiking Project Data API

Hiking Project provides a simple API with access to certain limited data. All of the data returned by the API is already available on publicly available pages on the Hiking Project site. Returned data is json.

```
Method: getTrails
Returns trails for a given query.

Required Arguments:

key - Your private key

lat - Latitude for a given area

lon - Longitude for a given area

Optional Arguments:

maxDistance - Max distance, in miles, from lat, lon. Default: 30. Max: 200.

maxResults - Max number of trails to return. Default: 10. Max: 500.

sort - Values can be 'quality', 'distance'. Default: quality.

minLength - Min trail length, in miles. Default: 0 (no minimum).

minStars - Min star rating, 0-4. Default: 0.


Method: getTrailsById
Returns trails for given IDs.

Required Arguments:

key - Your private key

ids - one or more trail IDs, separated by commas



```