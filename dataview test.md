---
uid: 2918c4a6-800f-4c0c-8845-628e9741592c
---
```dataview
LIST FROM #תואר WHERE !contains(uni_subjects,"אינפי") AND !contains(uni_subjects,"אלגברה") AND !contains(uni_subjects,"מושגי-יסוד-במתמטיקה")
```
```dataview
LIST WHERE contains(uni_subjects,"אלגברה") SORT length(uni_subjects) DESC
```
