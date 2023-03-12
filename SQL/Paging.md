To implement paging in view that's contains multiple rows for each product we can use DENSE_RANK() to give each unique product a unique number.
``` sql
SELECT * FROM (
SELECT *, DENSE_RANK() OVER ( ORDER BY CreatedOn, Id ) AS PropertyNumber
FROM prop.PropertiesView
WHERE (Title LIKE '%house%' OR Description LIKE '%house%')
) AS PropertiesWithNumber
WHERE PropertyNumber BETWEEN 16 AND 20
```
we should keep in mind that the order on which Ranking use should be same as the order of the view
#sql