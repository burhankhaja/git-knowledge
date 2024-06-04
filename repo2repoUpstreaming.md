# SYNCING REPO TO REPO CHANGES BETWEEN ORIGINAL AND THE IMPORTED ONE

`Let's say there is a public CLASS_REPO and you imported it privately and created INSTANCE_REPO, now the CLASS_REPO after you finished importing it got lot of changes. Since your INSTANCE_REPO
doesn't contain those changes, here is how you sync them:`

- Step 1: Assuming repo is cloned locally, if not clone it first and then change directory into the the location:
  ```bash
  cd INSTANCE_REPO/
  ```
- Step 2: Add your imported repository (CLASS_REPO)as remote
```bash
git remote add upstream https://github.com/CLASS_REPO
```
- Step 3: Fetch updates from the CLASS_REPO, without merging them
```bash
git fetch upstream # since CLASS_REPO is set as upstream
```

- Step 4: Merge updates in your local INSTANCE_REPO
```bash
git merge upstream/main
# OR == # git merge upstream/master
```

- Step 5: Push updates to the live INSTANCE_REPO
```bash
git push origin main
# OR # git push origin master

```

## SOURCE : https://www.phind.com/search?cache=qp6ml73s4nqtovsax8pxe7a9&source=sidebar
