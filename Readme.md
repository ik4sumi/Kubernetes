# Kubernets笔记

## 基础信息
- [官方文档](https://kubernetes.io/docs/home/)
- [中文文档](https://www.kubernetes.org.cn/kubernetes)
- [Nautilus文档](https://docs.nationalresearchplatform.org/userdocs/start/quickstart/)
- 我们的project名：`yelan-neuro`

## 常用命令

### Pod 相关命令
-  以某个yaml为模板建立pod: `kubectl create -f ./<xxxxx>.yaml`
-  查看某个project下的所有pod: `kubectl get pods -n <project_name>`
-  详细查看某个pod的信息: `kubectl get pods <pod_name> -n <project_name> -o wide`
-  执行某个资源的yaml文件: `kubectl apply -f ./<xxxxx>.yaml`
-  删除某个pod: `kubectl delete pod <pod_name> -n <project_name>`
-  用对应yaml删除某个pod: `kubectl delete -f ./<xxxxx>.yaml`
-  查看某个pod的详细信息: `kubectl describe pod <pod_name> -n <project_name>`
-  访问某个pod的shell: `kubectl exec -it <pod_name> -n <project_name> -- /bin/bash`
-  查看某个pod的日志: `kubectl logs <pod_name> -n <project_name>`

### Deployment 相关命令
-  以某个yaml为模板建立deployment: `kubectl create -f ./<xxxxx>.yaml`
-  查看某个project下的所有deployment: `kubectl get deployment -n <project_name>`
-  详细查看某个deployment的信息: `kubectl get deployment <deployment_name> -n <project_name> -o wide`
-  查看某个deployment下所有的pod: `kubectl get pods -n <project_name> -l app=<deployment_name>`