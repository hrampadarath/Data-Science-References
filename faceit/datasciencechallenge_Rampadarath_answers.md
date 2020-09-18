## FACEIT - Data Challenge
#### Hayden Rampadarath

### Q1 - SQL Challenge

#### 1.

```SQL
# mysql
select count(distinct match_id) from match_played
where YEAR(created_at) = 2018 and membership = 'premium'
group by YEAR(created_at);

```
### 2.

``` SQL
# mysql
select faction, winner, count(distinct match_id) wins, group_concat(user_id) id
from match_played
where faction = winner
group by faction
having wins >=3;
```
