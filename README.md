Mod of submodules of mods used on Blocky Survival

Installing
==========

1. `git clone https://github.com/BlockySurvival/bls_mods.git`
2. `cd bls_mods`
3. `git submodule update --init --recursive`

Updating your mods repo
=======================

1. `git pull`
2. `git submodule sync`
3. `git submodule update --recursive --init`
 
Setting up your local mods repo to push updates
===============================================

Note: It is preferable to *not* make updates directly on the Blocky Survival server.

1. `git remote add github git@github.com:BlockySurvival/bls_mods.git`

Upgrading a subrepo
===================

1. `git submodule update --recursive --remote SUBREPO_NAME`
2. `git add SUBREPO_NAME .gitmodules`
3. `git commit -m 'updated SUBREPO'`
4. `git push github master`

Upgrading all subrepos
======================

1. `git submodule update --recursive --remote`
2. `git add .`
3. `git commit -m 'updated all'`
4. `git push github master`

Adding a new subrepo
====================

1. `git submodule add http://path/to/git/repo`
2. `git commit -m 'added new repo'`
3. `git push github master`

Making changes inside a subrepo
===============================

1. `cd subrepo`
2. e.g. `git remote add github git@github.com:BlockySurvival/....`
3. make changes
4. `git add changed_file`
5. `git commit -m 'changed something'`
6. `git push github HEAD:master`
7. `cd ..`
8. `git add subrepo`
9. `git commit -m 'updated subrepo'`
10. `git push github master`
