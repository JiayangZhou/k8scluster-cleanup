# k8scluster-cleanup
A native Kubernetes CronJob that would periodically clean up a cluster, and discard unused namespaces.

It filters to-be-deleted namespaces based on criteria specified in the helm's value file, mainly the status of pods as well as their ages in a namespace. 

The functionality also provides a way to protect against accident deletion, protected namespace names can be specified in the helm's value file.
