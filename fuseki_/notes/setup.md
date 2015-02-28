## Hosting
* Repo on GitHub
* Served by OpenShift
  * www.thoughtcatchers.org -> fuseki-hyperdata.rhcloud.com
  * (www.hyperdata.it -> seki-hyperdata.rhcloud.com)

## DNS Setup
* Gandi domains, CNAME entries added pointing to OpenShift
* OpenShift aliases added

## Repo Setup
* locally, using /home/danny/seki2
* Created github repo danja/seki2
* Created github repo danja/seki2-fuseki (for OpenShift-flavoured Fuseki)
* synced github & OpenShift (www.thoughtcatchers.org -> fuseki-hyperdata.rhcloud.com)
  * see https://forums.openshift.com/how-to-keep-a-github-repository-and-an-openshift-repository-in-sync

-------------------------
* git submodule add https://github.com/danja/seki2-fuseki.git fuseki
  * see http://blog.joncairns.com/2011/10/how-to-use-git-submodules/
// bah, need OpenShift config in root
* Created github repo danja/seki2-openshift
* git submodule add https://github.com/danja/seki2-openshift.git .openshift

// grrr!
git remote add openshift ssh://521b08db4382ece7830001d5@fuseki-hyperdata.rhcloud.com/~/git/fuseki.git/
//////////// Starting again - silly me, foowiki was effectively a submodule of fuseki (not seki2) were probs setting up 

Deleted/re-created repos seki2, fuseki
git submodule add https://github.com/danja/seki2-fuseki.git fuseki
git submodule add https://github.com/danja/seki2-openshift.git .openshift
git submodule add https://github.com/danja/foowiki.git foowiki

git remote add openshift ssh://54f192474382ecdefc00011e@seki2-hyperdata.rhcloud.com/~/git/seki2.git/

check logs:
ssh in, 
cd $OPENSHIFT_LOG_DIR 


