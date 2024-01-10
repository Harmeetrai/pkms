# <% moment(tp.file.title,'YYYY-MMMM').format("MMMM, YYYY") %>

[[<% tp.date.now("YYYY-MMMM", -1) %>|Previous Month]] | [[<% tp.date.now("YYYY-MMMM", 1) %>|Following Month]]

> [!METADATA]-
> Created:: [[<% tp.date.now('YYYY-MM-DD') %>]] <% tp.date.now('HH:mm') %>
> Updated:: <% tp.date.now('YYYY-MM-DD HH:mm') %>
> ID:: <% tp.date.now('YYYYMMDDHHmmss') %>
> tags:: #log/journal #log/monthly 

```dataview
LIST 
From "Journal/<% tp.date.now("YYYY")%>/<% tp.date.now("MM-MMMM")%>"
WHERE 
	contains(file.name, "W")
sort file.name asc
```



