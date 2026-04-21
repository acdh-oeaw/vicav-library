VICAV Library
=============

This repository contains common data that is shared between the VICAV projects

* Bibliography
* Geo data
* Rendition instructions

Contents description
--------------------

Geo data contains place names in different writings and languages used elsewhere in the VICAV projects.  
One such place is the bibliography where the geo coordinates are added to the Zotero export by looking up the names in Zotero in the geo data file.

In `vicav_rendition.xml` we suggest a rendering for TEI tags used in our data.

Usage
-----

We include this library as a git submodule in other VICAV project data repositories.

If you've cloned the project repo but don't have the submodule yet do `git submodule init vicav-library` and `git submodule update vicav-library`

A git submodule always references revision identified by its hash. Updates need to be done explicitly by updating such submodules. 
When you want to update sth in vicav-library:
If you're in the project repository where the submodule is included:
* Enter submodule with `cd vicav-library` then do  `git switch main` and `git pull origin main`  to make sure you're working in the up-to-date main branch.
* Make edits, commit, and push **inside submodule**

After having committed and pushed changes to vicav-library do the following steps:

* change to the project data repository
* `git submodule update --remote`: This fetches the updated version of vicav-library
* `git add vicav-library`: set the submodule to the latest commit of vicav-library
* `git commit -m 'updating vicav-library'` and `git push` 
