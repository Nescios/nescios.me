---
title: Notes
---

## Graph of Git flow

**Git flow graph**
```mermaid
  gitGraph
    commit
    branch develop
    checkout develop
    commit
    branch feature
    checkout feature
    commit
    commit
    checkout develop
    merge feature
    branch release
    checkout release
    commit
    checkout develop
    merge release
    checkout main
    merge release
    branch hotfix
    checkout hotfix
    commit
    checkout develop
    merge hotfix
    checkout main
    merge hotfix
    checkout develop
    commit
```

**Tag naming convention:**
```bash
v0.1.0
v<major>.<minor>.<patch>
```

---

## Use Git Large File Storage

For large files, [git-fls](https://git-lfs.github.com/) is a good solution.

  
  ```bash
  brew instal git-lfs
  ```
  
  ---

  ## Usefull Api

- [Bored API](https://github.com/drewthoennes/Bored-API) - A simple API for finding things to do.
- [JSONPlaceholder](https://jsonplaceholder.typicode.com/) - A fake API that supports JSON and CRUD operations.
