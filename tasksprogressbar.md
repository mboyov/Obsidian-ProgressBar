---
total: 4
incomplete: 2
completed: 2
---


```dataviewjs
let myPage = dv.current()
    let total = myPage.total;
    let status = ((myPage.completed / myPage.total) * 100).toFixed();
    const progress = "![pb|500](https://progress-bar.dev/" + status + "/?scale=" + "100" + "&width=400)";
    dv.header(3, "Objectif du jour"); dv.paragraph(progress);
``` 

### Tasks

- [x] 1
- [x] 2
- [ ] 3
- [ ] 4