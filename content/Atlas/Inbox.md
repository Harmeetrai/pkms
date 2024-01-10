# The Inbox
---
This view looks at the 20 newest notes in your **Encounters** folder. As you process each note, make connections, add details, move them to the best folder,  and delete everything that no longer sparks ✨. 

``` dataview
TABLE WITHOUT ID
 file.link as "Encounters and new notes",
 (date(today) - file.cday).day as "Days alive"

FROM "Encounters" and -#on/readme 

SORT file.cday asc

LIMIT 20
```
