To implement paging in view that's contains multiple rows for each product because of joining we can use DENSE_RANK() to give each unique product a unique number based on it's id.
``` sql
SELECT 
	* 
FROM (
	SELECT 
		*,
		DENSE_RANK() OVER ( ORDER BY CreatedOn, Id ) AS ProductNumber
	FROM 
		prop.ProductsView
	WHERE 
		(Title LIKE '%X%' OR Description LIKE '%X%')
	) AS ProductsWithRank
WHERE 
	ProductNumber
BETWEEN 16 AND 20
ORDER BY 
	CreatedOn, Id
```
**we should use the same order in the ranking and query.**

#sql