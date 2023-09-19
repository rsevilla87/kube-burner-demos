## Running kube-burner

Run these commands

```shell
kube-burner init -c config.yml

oc get ns | grep ask-ocp-admin
oc get deploy -n ask-ocp-admin-4
oc get deploy -n ask-ocp-admin -l kube-burner-job=ask-ocp-admin

# Set gc to true and re-run
kube-burner init -c config.yml
```

Demonstrate that all namespaces were garbage collected at the end of the run

```shell
oc get ns | grep ask-ocp-admin
```