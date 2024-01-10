#  <% moment(tp.file.title,'YYYY-MM-DD').format("dddd, MMMM DD, YYYY") %>

> [!METADATA]-
> Created:: [[<% tp.date.now('YYYY-MM-DD') %>]] <% tp.date.now('HH:mm') %>
> Updated:: <% tp.date.now('YYYY-MM-DD HH:mm') %>
> ID:: <% tp.date.now('YYYYMMDDHHmmss') %>
> tags:: #log/journal #log/daily 

---
week: [[<% tp.date.now("YYYY-[W]W", 0, tp.file.title, "YYYY-MM-DD") %>]]
month: [[<% tp.date.now("YYYY-MMMM", 0, tp.file.title, "YYYY-MM-DD") %>]]
year: [[<% tp.date.now("YYYY", 0, tp.file.title, "YYYY-MM-DD") %>]]

<< [[<% fileDate = moment(tp.file.title, 'YYYY-MM-DD').subtract(1, 'd').format('YYYY-MM-DD') %>|Yesterday]] | [[<% fileDate = moment(tp.file.title, 'YYYY-MM-DD').add(1, 'd').format('YYYY-MM-DD') %>|Tomorrow]] >>

---

