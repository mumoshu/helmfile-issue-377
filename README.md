```
$ helm tiller run -- ../helmfile --environment dev diff
Installed Helm version v2.10.0
Installed Tiller version v2.10.0
Helm and Tiller are the same version!
args=../helmfile --environment dev diff
Starting Tiller...
Comparing environment /Users/kuoka-yusuke/go/src/github.com/roboll/helmfile/testdir/charts/environment
********************

	Release was not present in Helm.  Diff will show entire contents as new.

********************
2018/10/03 11:13:50 Error: Found duplicate key "default, configuration, ConfigMap (v1)" in manifest
default, configuration, ConfigMap (v1) has been added:
-
+ # Source: environment/templates/configmap.yaml
+ kind: ConfigMap
+ apiVersion: v1
+ metadata:
+   name: configuration
+ data:
+   BASE_URL: DEV_ENV_BASEURL
+   BACKEND_DEBUG: DEV_ENV_DEBUG

Stopping Tiller...
```
