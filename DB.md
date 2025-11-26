---
publish: false
---
```dataview
TABLE name, uid
FROM #תואר 
WHERE contains(uni_subjects,"אינפי") AND !contains(file.tags,"#סיכומים") AND !contains(file.tags,"גליונות")
```
