## Cheatsheet for working with dates

### Sample DB snapshot - Orders_archive
|order_id | order_state | created_at               |
|:-------:|:-----------:|:------------------------:|
| abc123  | ordered     | 2015-10-06T11:54:00.000Z |
| cse456  | declined    | 2015-10-06T10:54:00.000Z |
| asd675  | ordered     | 2015-10-05T04:44:00.000Z |
| asd675  | ordered     | 2015-10-05T03:54:00.000Z |
| asd675  | ordered     | 2015-10-03T11:54:00.000Z |
| qwe345  | ordered     | 2015-10-02T11:54:00.000Z |

>nb: the created_at value is a timestamp type.

To easily work with timestamp values, we can use the `date_trunc` function, to round off a time stamp to a more appropriate time-based value.

```sql
DATE_TRUNC('[interval]', time_column)
```
where **time_column** is the timestamp based column of hte table and **interval** is the desired precision level.

Interval could be second, minute, hour, day, week, month, year...

For the sample DB snapshot above, to get the total count of orders placed in a day:

```sql
SELECT
 count(created_at) as orders_placed,
 date_trunc('day', created_at) as date_placed,
 state as order_state
FROM orders_archive
WHERE state = 'ordered'
GROUP by date_trunc('day', created_at), state
ORDER by date_trunc('day', created_at) desc;
```
