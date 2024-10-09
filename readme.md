# Custom archlinux packages

It's a web-hosted directory, which contains:

- pacman packages (e.g. *pkgname-1.0.0-1-any.pkg.tar.zst*)
- database file (eg. *jurepo.db, jurepo.db.tar.gz*)
- files file (eg. *jurepo.files, jurepo.files.tar.gz*)



You [create packages](https://wiki.archlinux.org/title/Creating_packages) by following arch wiki :)
You build them with `makepkg -s`, which outputs a package .pkg.tar.gz
Copy them into repository
Update repository list with `repo-add <reponame>.db.tar.gz <packagename>`

That's it.



## Build package

Create and/or modify the PKGBUILD file.
Bump the pkgrel versioning number.
Run `makepkg` within the same directory.



## Add package to repository

Copy package (.pkg.tar.zst) into the repository.
Update databases with `repo-add <reponame>.db.tar.gz <packagename>`



## Push the updated repo

git commit, git push. Its all being used locally at the moment (repo is downloaded from github when done).
