# MicroK8S

# Notes

## Frequently used commands

```
kubectl apply -f spore-drive.yml --output=yaml

kubectl delete deployment nginx
kubectl delete job spore-drive-zk918
kubectl stop pod nginx-676b6c5bbc-pg2
kubectl delete pod -l app=myapp

kubectl logs spore-drive-grmcz
kubectl logs deployment.apps/shield --all-containers -tail=50

kubectl config get-contexts
kubectl config use-context microk8s

kubectl describe pod rabbitmq-0


kubectl get deployments
kubectl get namespaces -o name

kubectl get deployments <NAME>
kubectl scale deployment eridani-d --replicas=0
kubectl edit deployment eridani-d

kubectl get -o yaml job spore-drive-grmcz
kubectl get pods
kubectl get nodes
kubectl get events

kubectl exec --stdin --tty rabbitmq-0 -- /bin/bash
kubectl exec -n <name space here> <pod-name>  -it -- /bin/sh

```


```
microk8s ctr images ls
microk8s reset
microk8s status --wait-ready
microk8s kubectl get nodes
microk8s kubectl get services
microk8s kubectl create deployment nginx --image=nginx
microk8s enable dns
microk8s enable hostpath-storage
microk8s enable rbac
microk8s.inspect
```


```
docker image prune
docker run --rm -it --name sporedrive localhost:32000/discovery-challenge/sporedrive:dev bin/bash
docker rmi $(docker images | grep "^<none>" | awk "{print $3}")
```

# Links

- MicroK8s Tutorials -- https://microk8s.io/docs/tutorials
- MicroK8s How To guides -- https://microk8s.io/docs/how-to
- Original repo --  https://github.com/loft-orbital/challenge-sre
- To get the kinds of objects in Kubernetes --  https://stackoverflow.com/questions/53053888/where-is-the-complete-list-of-kubernetes-objects
- to enable local registry in microk8s -- https://microk8s.io/docs/registry-built-in
- microk8s command reference -- https://microk8s.io/docs/command-reference
- kubernetes job -- https://kubernetes.io/docs/concepts/workloads/controllers/job/
- microk8s troubleshooting -- https://microk8s.io/docs/troubleshooting
- delete pods, delete depoyments -- https://stackoverflow.com/questions/40686151/kubernetes-pod-gets-recreated-when-deleted
- microk8s local registry -- https://microk8s.io/docs/registry-images
- How to use the built-in registry -- https://microk8s.io/docs/registry-built-in
- ttlSecondsAfterFinished -- https://stackoverflow.com/questions/61654433/helm-upgrade-failed-cannot-patch-with-kind-job-by-update-field-image
- Determine the Reason for Pod Failure -- https://kubernetes.io/docs/tasks/debug/debug-application/determine-reason-pod-failure/
- Delete all PODS -- https://www.baeldung.com/ops/kubernetes-delete-all-pods
- How to work with a private regist -- https://microk8s.io/docs/registry-private
- How to Clean Up Old Kubernetes Jobs -- https://www.howtogeek.com/devops/how-to-clean-up-old-kubernetes-jobs/
- A Comprehensive Guide to Kubectl Stop Deployment -- https://thelinuxcode.com/kubectl-stop-deployment/
- AMQ module this assignment uses  --  https://github.com/streadway/amqp
- Kubernetes jobs -- https://kubernetes.io/docs/concepts/workloads/controllers/job/
- Understanding init containers -- https://kubernetes.io/docs/concepts/workloads/pods/init-containers/
- guide covers a number of topics related to RabbitMQ CLI tools usage -- https://www.rabbitmq.com/docs/cli
- Pika Docs -- https://pika.readthedocs.io/en/stable/examples.html
- Well-Known Labels, Annotations and Taints -- https://kubernetes.io/docs/reference/labels-annotations-taints/
- Working with gzip Compression -- https://reintech.io/blog/a-guide-to-gos-compress-package-working-with-compression-algorithms
- Resource units in Kubernetes -- https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/
- KEDA is a Kubernetes based Event Driven Autoscaler. -- https://microk8s.io/docs/addon-keda
- Create the HorizontalPodAutoscaler -- https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale-walkthrough/#create-horizontal-pod-autoscaler
- DataPower horizontal pod autoscaling with MicroK8s -- https://community.ibm.com/community/user/integration/blogs/pedro-busko/2021/06/03/datapower-horizontal-pod-autoscaling-with-microk8s

