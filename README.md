# autogitdeployment
How to automatically deploy project to server on pushing to git


<ul>Go to server create site.git (mkdir site.git)</li>


<li>	Cd site.git </li>


<li> git init --bare </li>

<li>	--bare means that our folder will have no source files, just the version control. </li>

<li>	cat > post-receive (type what is below 2 lines) </li>

<li>	#!/bin/sh </li>

<li>	git --work-tree=/var/www/domain.com --git-dir=/var/repo/site.git checkout -f </li>

<li>	chmod +x post-receive </li>

<li>	git remote add beta ssh://user@mydomain.com/var/repo/beta.git </li>

</ul>

//commit and test

