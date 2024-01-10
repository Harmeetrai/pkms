```dataview
table without id
 ("![](" + poster + ")") as Poster,
 file.link as Title,
 year as Year, director as Director,
 "⭐ " + scoreImdb as "⭐ IMDB",
 rating, genre
from #movie 
where contains(status, "watched") AND rating > 7
SORT file.ctime DESC
```
