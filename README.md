# iri-n1ql
These are N1QL for IRI equation values. 



### INSERT  
**for 100m segments**  
`INSERT INTO iroads (KEY, VALUE) VALUES ("iri-equation-data-100",
      { "key":"iri-equation-data-100","dataType": "iri_equation", "m": 4.40, "c": 2, "segmentLength":100}) RETURNING *;`  
**for 300m segments**  
`INSERT INTO iroads (KEY, VALUE) VALUES ("iri-equation-data-300",
      {  "key":"iri-equation-data-300","dataType": "iri_equation", "m": 4.40, "c": 2, "segmentLength":300}) RETURNING *;`  
**for 500m segments**  
`INSERT INTO iroads (KEY, VALUE) VALUES ("iri-equation-data-500",
      {  "key":"iri-equation-data-500","dataType": "iri_equation", "m": 4.40, "c": 2, "segmentLength":500}) RETURNING *;`  
      
 ### UPDATE  
 **for 100m**  
 `UPDATE iroads USE KEYS "iri-equation-data-100" SET c = 2, m=3 RETURNING *;`    
 **for 300m**  
 `UPDATE iroads USE KEYS "iri-equation-data-300" SET c = 2, m=3 RETURNING *;`    
 **for 500m**  
 `UPDATE iroads USE KEYS "iri-equation-data-500" SET c = 2, m=3 RETURNING *;`  
  
 ### SELECT  
 **select for specific length**  
 `select c,m,segmentLength from iroads where dataType="iri_equation" and segmentLength=100;`  
 **selecet all**  
 `select * from iroads where dataType="iri_equation"`  
 
 ### DELETE  
 **delete specific**  
 `delete from iroads where dataType="iri_equation" and segmentLength=100;`  
 **delete all**  
 `delete from iroads where dataType="iri_equation";`  
