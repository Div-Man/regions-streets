# regions-streets

```sql
SELECT 
        countries.name_city, 
        regions.name_region, 
        cities_and_areas.name_city_and_areas,
      locality.name_locality,
     streets.name_street
       FROM countries 
      INNER JOIN regions ON regions.country_id = countries.id 
      INNER JOIN cities_and_areas ON cities_and_areas.region_id = regions.id 
      INNER JOIN locality ON locality.cities_and_areas_id = cities_and_areas.id  
      INNER JOIN streets ON streets.locality_id = locality.id 
     
      ORDER by streets.name_street
   ```   
 
  ```sql
  
  SELECT 
        countries.name_city, 
        regions.name_region, 
        cities_and_areas.name_city_and_areas,
      locality.name_locality,
     streets.name_street
       FROM countries 
      INNER JOIN regions ON regions.country_id = countries.id 
      INNER JOIN cities_and_areas ON cities_and_areas.region_id = regions.id 
      INNER JOIN locality ON locality.cities_and_areas_id = cities_and_areas.id  
      INNER JOIN streets ON streets.locality_id = locality.id 
     
     WHERE streets.name_street = 'Мира Улица' AND locality.name_locality = 'Хомуты Хутор'
      ORDER by streets.name_street
      
     ``` 
