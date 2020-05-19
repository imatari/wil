## Things I learned from the course<br>_and some things outside of the course along the way_

### from the course
- URL to course
    - https://youtu.be/qw--VYLpxG4
- Introduced to **https://mockaroo.com**
    - It can produce a table of mock data for you to practice your database query skills on.
- PSQL Commands
    - **`\i` Execute Commands From a File**
        - example: **`\i /home/user/Desktop/cars.sql`**
    - **`\x` expanded display**
        - Is the output from your query too wide? Use this to transpose the output

- The following will take the result from a query and output it to a file named results.csv with the delimiter as a comma and include the header row.
```sql
\copy 
    (SELECT *
    FROM person
    LEFT JOIN car
        ON car.id = person.car_id) 
to '/home/user/Desktop/results.csv' delimiter ',' csv header; 
```


- The instructor used draw.io for illustrating a point. (_I like draw.io and it's nice to see others using it too._)


### outside the course
- creating a user with admin rights (_in Ubuntu_)
    - https://medium.com/coding-blocks/creating-user-database-and-adding-access-on-postgresql-8bfcd2f4a91e
- PSQL Command
    - **`\c`**
        - this by itself will tell you  
            1. what database you are in/connected to 
            2. who you 

### Practical Resources
- 17 Practical psql Commands That You Don’t Want To Miss
    - https://www.postgresqltutorial.com/psql-commands/


