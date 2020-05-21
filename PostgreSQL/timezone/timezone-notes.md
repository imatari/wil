## Postgres natively on Xubuntu
### Example 01
![Postgres returns the timezone you are in][ex01]  
Illustrates a date being cast into a date time with timezone
* There is no time given and as a result, Postgres returns a timestamp of `00:00:00` 
* I'm in California and at the first day of the year 2000, we are in standard time at `-08`
### Example 02
![from standard to daylight saving][ex02]  
Demonstrates Postgres' awareness of when Daylight Saving Time happens  
For the year 2004, California changed from a timezone of `-08` to `-07` when we went from April 4 to April 5  
**source:** https://www.timeanddate.com/time/zone/usa/los-angeles

## Postgres spun up from an image on Docker
Here is the instruction used to spin up my instance in Windows 10 with Powershell:
```
docker volume create pg-sb

docker run --name pg-sandbox `
-e POSTGRES_USER=matari `
-e POSTGRES_PASSWORD=cheeseburger `
-p 5432:5432 `
--mount source=pg-sb,target=/var/lib/postgresql/data `
-d postgres
```
### Example 03
![Postgres inside Docker][ex03]
from an instance of Postgres inside Docker, the Linux environment that Postgres sits in has a time zone of `+00`, Coordinated Universal Time (_UTC_)

[ex01]: images/pg-xubuntu.jpg
[ex02]: images/time-change-2004.jpg
[ex03]: images/pg-docker.jpg
