
```dataview 
TABLE 
length(filter(endswith(file.inlinks.file.folder, "DATA/data points"), 
	(x) => (x))) AS "related data points", 
length(filter(endswith(file.outlinks.file.folder, "DATA/codes"), 
	(x) => (x)))  AS "related codes" 
FROM "DATA/codes"
WHERE contains(file.inlinks.file.folder, "data points")
SORT length(filter(endswith(file.inlinks.file.folder, "DATA/data points"), 
	(x) => (x))) DESC 
```


