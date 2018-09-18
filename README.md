# autogitdeployment
How to automatically deploy project to server on pushing to git


•	Go to server create site.git (mkdir site.git)
•	Cd site.git
•	git init --bare
•	--bare means that our folder will have no source files, just the version control.
•	cat > post-receive (type what is below 2 lines)
•	#!/bin/sh
•	git --work-tree=/var/www/domain.com --git-dir=/var/repo/site.git checkout -f
•	chmod +x post-receive
•	git remote add beta ssh://user@mydomain.com/var/repo/beta.git

//commit and test

