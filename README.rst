========
Deployer
========

Some vague ruminations on the flows we'd like to see from a dev point
of view.

Dev experience
==============

 $ # hack hack hack
 $ git commit . -m 'my awesome commits'
 $ git push buildbot
   # wait a bit
  To git@gitproxy:rip747/cfwheels.git
! [rejected]        master -> master (non-fast forward)
error: failed to push some refs to 'git@buildbot:my_awesome_project.git'
  - your code didn't compile/failed some tests/smells funny
 $ # grumble grumble
 $ # hack hack hack
 $ git commit . -m 'fix up my awful commits'
 $ git push buildbot
  # 



Author
======
Mark Wotton @mwotton
