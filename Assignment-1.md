SQL assignment:

(f and t mean false and true, respectively)

Please share query and output for each:

Questions:

1. What is the time period used?
  
```sql
select MIN(date), MAX(date) from airbnb_calendar;
```
<img src = "./media/time_period.png">


2. How many properties have duplicate entries? Remove duplicate rows (say a row appears 3 times, remove 2 and keep 1)

```sql
select count(distinct listing_id), count(distinct date), count(distinct available), count(distinct price) from airbnb_calendar;
```

<img src = "./media/distinct_props.png">

```sql
SELECT distinct listing_id,date,available,price FROM airbnb_calendar;
```

<img src = "./media/distinct_select.png">
3. For each property, find out the number of days the property was available and not available (create a table with listing_id, available days, unavailable days and available days as a fraction of total days)

4. How many properties were available on more than 50% of the days? How many properties were available on more than 75% of the days?

5. Create a table with max, min and average price of each property

6. Extract properties with an average price of more than $500
