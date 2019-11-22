# clouddriver-openstack

This is a work-in-progress revival of the Spinnaker OpenStack clouddriver provider.  It is not complete.

To use this, check out a `master` version of `spinnaker/clouddriver`, check this repo out into a directory under it, and apply this patch:

```
diff --git a/settings.gradle b/settings.gradle
index 57aa7d319..a796d3f0d 100644
--- a/settings.gradle
+++ b/settings.gradle
@@ -25,7 +25,8 @@ def cloudProviderProjects = [
   'dcos': [':clouddriver-dcos'],
   'gce': [':clouddriver-consul', ':clouddriver-google', ':clouddriver-google-common'],
   'kubernetes': [':clouddriver-kubernetes', ':clouddriver-kubernetes-v1', ':clouddriver-kubernetes-v2', ':clouddriver-docker'],
-  'oracle': [':clouddriver-oracle']
+  'oracle': [':clouddriver-oracle'],
+  'openstack': [':clouddriver-openstack']
 ]
 cloudProviderProjects.put('gcp', cloudProviderProjects['appengine'] + cloudProviderProjects['gce'] + cloudProviderProjects['kubernetes'])
 cloudProviderProjects.put('titus', cloudProviderProjects['aws'] + ':clouddriver-titus')
```
