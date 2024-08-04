# Requête imbriquée
```sql
SELECT *
FROM(
  SELECT 
    prix_sp98 ,
    ville,
    adresse ,
    ROUND(
      ST_DISTANCE(
        ST_GEOGPOINT(0.225331 , 49.157331), 
        ST_GEOGPOINT(longitude , latitude)
      )/1000 , 2) distance_en_km ,
    code_departement ,
  FROM fr_carburants.carburants
  WHERE code_departement="14"
  AND prix_sp98 IS NOT NULL
  ORDER BY prix_sp98 ASC
)WHERE distance_en_km < 20; */
```
# Requpete CTE (Common Table Expression)
```sql
WITH stations_sp98_14 AS (
  SELECT 
    prix_sp98 ,
    ville,
    adresse ,
    ROUND(
      ST_DISTANCE(
        ST_GEOGPOINT(0.225331 , 49.157331), 
        ST_GEOGPOINT(longitude , latitude)
      )/1000 , 2) distance_en_km
  FROM fr_carburants.carburants
  WHERE code_departement="14"
  AND prix_sp98 IS NOT NULL
  -- ORDER BY prix_sp98 ASC
)
SELECT *
FROM stations_sp98_14
WHERE distance_en_km < 20;
```
# Requête finale
```sql
SELECT
  adresse ,
  ville ,
  CONCAT(adresse , ', ' , code_postal , ' ' , ville) adresse_complete ,
  ROUND(prix_sp98 , 3) prix_sp98,
  ROUND(ST_DISTANCE(
    ST_GEOGPOINT(0.225331 , 49.157331), 
    ST_GEOGPOINT(longitude , latitude) )/1000 , 1) distance_km
FROM fr_carburants.carburants
WHERE code_departement = '14'
  AND prix_sp98 IS NOT NULL
ORDER BY distance_km ASC;
```