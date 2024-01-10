# <% moment(tp.file.title,'[[YYYY]]-[W]WW').format("[Week] WW, [[YYYY]]") %>

[[<% tp.date.now("YYYY-[W]WW", -7) %>|Previous Week]] | [[<% tp.date.now("YYYY-[W]WW", 7) %>|Following Week]]

> [!METADATA]-
> Created:: [[<% tp.date.now('YYYY-MM-DD') %>]] <% tp.date.now('HH:mm') %>
> Updated:: <% tp.date.now('YYYY-MM-DD HH:mm') %>
> ID:: <% tp.date.now('YYYYMMDDHHmmss') %>
> 
> tags:: #log/journal #log/weekly

```dataview
LIST 
From #log/journal 
WHERE 
	date(file.name).year = <% tp.date.now("YYYY")%> AND date(file.name).weekyear = <% tp.date.now("ww")%>
sort file.name asc
```

# Plans for this week
---
# Reflection
---
## Good things that happen

## Bad things that I need to learn from

# For Next Week
---
