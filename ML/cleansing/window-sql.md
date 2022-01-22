
-- assign as single row number 1,24,
SELECT city,dock_count,row_number() OVER (PARTITION BY city ORDER BY dock_count desc ) from station;


-- assign rank on overall data if 24 diffrent values for dock_count overall then it will range from 1 to 24 
SELECT city,dock_count,rank() OVER (PARTITION BY city ORDER BY dock_count desc ) from station;

-- assign rank on overall partion data if 7 diffrent values for dock_count in a given city say overall then it will range from 1 to 24 
SELECT city,dock_count,dense_rank() OVER (PARTITION BY city ORDER BY dock_count desc ) from station;

-- assgin percentiles value by dividing say 5 rankk in given partition 0,.25,.50,.75,1.0  
SELECT city,dock_count,percent_rank() OVER (PARTITION BY city ORDER BY dock_count desc ,'p') from station;

-- assgin percentiles value by dividing sa 7 2 , 4 , 1 of same value then .28 ,.85,1.0 will have respective values  
SELECT city,dock_count,cume_dist() OVER (PARTITION BY city ORDER BY dock_count desc ) from station;

-- assign a distribution number on overall cateogary 0- 100 assign quaritle
SELECT city,dock_count,ntile(4) OVER (PARTITION BY city ORDER BY dock_count desc ) from station;


-- assign a distribution number on overall cateogary 0- 100 assign quaritle
SELECT city,dock_count,first_value(name) OVER (PARTITION BY city ORDER BY dock_count desc 
RANGE BETWEEN
UNBOUNDED PRECEDING AND
UNBOUNDED FOLLOWING
) from station;

-- assign a distribution number on overall cateogary 0- 100 assign quaritle
SELECT city,dock_count,last_value(name) OVER (PARTITION BY city ORDER BY dock_count desc ) from station;


-- assign a distribution number on overall cateogary 0- 100 assign quaritle
SELECT city,dock_count,id,lag(id,1) OVER (PARTITION BY city ORDER BY id asc ) as prev_station_id from station;


-- assign a distribution number on overall cateogary 0- 100 assign quaritle
SELECT city,dock_count,id,lead(id,1) OVER (ORDER BY id asc ) as prev_station_id from station;

-- aggregation in partion
SELECT city,dock_count,avg(dock_count) OVER (PARTITION BY city) as overall_dock_count_by_city from station;


SELECT city,dock_count,count(*) OVER (PARTITION BY city) as overall_rows_count_for_a_given_city from station;

SELECT city,dock_count,MAX(dock_count) OVER (PARTITION BY city) as overall_rows_count_for_a_given_city from station;

SELECT city,dock_count,MIN(dock_count) OVER (PARTITION BY city) as overall_rows_count_for_a_given_city from station;


select name,lat,long,id,lead(id,1) OVER (ORDER BY id asc) as id1,lead(lat,1) OVER (ORDER BY id asc) as lat1,lead(long,1) OVER (ORDER BY id asc) as long1 from station

