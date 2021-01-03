# aion
Windows 10 Activity Timeline parser

## Artifact
Introduced in Windows 10 April 2019 Update, Windows 10 Timeline stores user's recent activity; opened apps, documents, visited sites. The activity is stored in a SQLite database `ActivitiesCache.db` located in `\Users\%profile name%\AppData\Local\ConnectedDevicesPlatform\L.%profile name%\`.

This artifact can help examiners determine and profile user activity during forensic investigations, as interesting features of the activities runtime are stored inside the database.

# Usage
Aion arguements are the Activity Timeline database and the timezone of the system that is being analyzed. 

By default aion will also display the UTC
```
aion.py -o report.csv ActivitiesCache.db Antarctica/Davis
```

One nice trick to list all available timezones:
```
for tz in pytz.all_timezones:
    print tz
```
