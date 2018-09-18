# autogitdeployment
How to automatically deploy project to server on pushing to git


<ul>Go to server create site.git (mkdir site.git)</li>


<li>	<code>Cd site.git</code> </li>


<li> <code>git init --bare </code></li>

<li>	--bare means that our folder will have no source files, just the version control. </li>

<li>	<code>cat > post-receive</code> (type what is below 2 lines) </li>

<li>	<code>#!/bin/sh</code> </li>

<li>	<code>git --work-tree=/var/www/domain.com --git-dir=/var/repo/site.git checkout -f </code> </li>

<li>	<code>chmod +x post-receive</code> </li>

<li>	go to working git folder and type <code>git remote add beta ssh://user@mydomain.com/var/repo/beta.git</code> </li>

</ul>

//commit and test

