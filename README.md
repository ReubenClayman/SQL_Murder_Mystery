SELECT * 
FROM crime_scene_report 
WHERE type = 'murder' 
AND city = 'SQL City' 
AND date = '20180115' 

Select * 
FROM person 
WHERE address_street_name = 'Northwestern Dr' 
ORDER BY address_number DESC 

Select * 
FROM person 
WHERE address_street_name = 'Franklin Ave' 
AND name LIKE '%ann%' 

SELECT * 
FROM interview 
WHERE person_id in (14887,16371) 

Select * 
FROM get_fit_now_check_in 
WHERE membership_id LIKE'%48Z%' 
AND check_in_date = 20180109 

SELECT * FROM get_fit_now_member 
WHERE id ='48Z7A' 
AND membership_status = 'gold' 

SELECT * 
FROM drivers_license AS dl 
INNER JOIN person AS p ON dl.id = p.license_id 
WHERE p.id in (67318,28819) 
AND plate_number LIKE '%H42W%' 

SELECT * 
FROM drivers_license as dl 
INNER JOIN person as p on dl.id = p.license_id 
WHERE p.id in (67318,28819) 
AND plate_number LIKE'%H42W%' 

SELECT * 
FROM interview where person_id = 67318 

SELECT dl.*,P.* 
FROM drivers_license as dl 
INNER JOIN person as p on dl.id = p.license_id 
WHERE dl.hair_color = 'red' 
AND dl.height <=67 
  AND dl.height >=65 
  AND dl.gender ='female' 
  AND dl.car_make = 'Tesla' 
  
SELECT fe.*,p.name 
FROM facebook_event_checkin as fe 
INNER JOIN person as p on p.id= fe.person_id 
WHERE event_name = 'SQL Symphony Concert' 
AND person_id in (78881,90700,99716)
