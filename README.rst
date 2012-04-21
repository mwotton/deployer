========
Deployer
========

Some vague ruminations on the flows we'd like to see from a dev point
of view.

Dev experience
==============

 $ # hack hack hack
 $ git commit . -m 'my awesome commits'
 $ git push buildbot master
   # wait a bit
  To git@buildbot:my_awesome_project.git
! [rejected]        master -> master (non-fast forward)
error: failed to push some refs to 'git@buildbot:my_awesome_project.git'
  - your code didn't compile/failed some tests/smells funny
 $ # grumble grumble
 $ # hack hack hack
 $ git commit . -m 'fix up my awful commits'
 $ git push buildbot master
  # wait
  Build accepted! Merging to github, tagging as #abcd1234, deploying to staging
 $ # go off and check staging
   # all good!

# less sure about this stuff, open to comment
 $ prod_deploy abcd1234
 $ # check - oh shit, we used the wrong creds! Abort, abort
 $ prod_rollback
 
Implementation notes
====================

this should work for multiple repos. might be nice to have a
new_channel script that automatically sets up a project with a cabal
file, buildbot endpoint, etc etc etc.



Author
======
Mark Wotton @mwotton
