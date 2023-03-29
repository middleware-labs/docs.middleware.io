## Verify Status for K8s Auto-Instrument Agent

Run this command to check the status of main daemonset component, which will be collecting data from your cluster

```
kubectl get daemonset/vision-data-collection -n mw-vision
```

Expected Output:
```
NAME                     DESIRED   CURRENT   READY   UP-TO-DATE   AVAILABLE   NODE SELECTOR   AGE
vision-data-collection   7         7         7       7            7           <none>          111s
```

If you have "N" number of k8s nodes, You should see "N" ready pods.

---------------

## Verify Status for K8s Infrastructure Agent

Run this command to check the status of main daemonset component, which will be collecting data from your cluster

```
kubectl get daemonset/mw-kube-agent -n mw-agent-ns
```

Expected Output:
```
NAME                     DESIRED   CURRENT   READY   UP-TO-DATE   AVAILABLE   NODE SELECTOR   AGE
mw-kube-agent            7         7         7       7            7           <none>          111s
```

If you have "N" number of k8s nodes, You should see "N" ready pods.






