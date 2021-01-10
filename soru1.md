```SQL
select * from `dsmbootcamp.irem_cakmakli.semi_structured_hw`;
select * from `dsmbootcamp.irem_cakmakli.semi_structured_hw_expected`;
select name,c.id,m.year, c.model
from `irem_cakmakli.semi_structured_hw`
cross join unnest(car) as car
cross join unnest(manufacture) as m
order by name desc, c.id;
```
