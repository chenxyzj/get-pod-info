# V2.0: 将创建命名空间放在yaml文件中
## 0. 更新了yaml文件
## 1. apply
``` kubectl apply -f ./dapi-test-pod.yaml  ```
## 2. 查看命名空间、查看pod
``` kubectl get ns ```
``` kubectl get pod -n dapi-test-api  ```
## 3. 查看容器日志
  - 方法1: 通过vscode的k8s扩展查看pod的log
  - 方法2: 通过命令查看日志
    ``` kubectl -n dapi-test-app logs dapi-test-pod ```
## 4. delete
``` kubectl delete -f ./dapi-test-pod.yaml  ```
## 5. 查看命名空间、查看pod已经删除
``` kubectl get ns ```
``` kubectl get pod -n dapi-test-api  ```

# V1.0: 测试通过Downward API传递pod信息给容器内应用

## 0. 创建测试的命名空间
``` kubectl create ns dapi-test-app ```
## 1. 编辑yaml文件

## 2. 应用
``` kubectl apply -f ./dapi-test-pod.yaml ```

## 3. 查看
  - 方法1: 通过vscode的k8s扩展查看pod的log
  - 方法2: 通过命令查看日志
        ``` kubectl -n dapi-test-app logs dapi-test-pod ```
## 4. 删除

    ``` 
    kubectl delete -f ./dapi-test-pod.yaml 
    kubectl delete ns dapi-test-app 
    ```

## 参考
[1]. https://blog.csdn.net/saga_gallon/article/details/92839589
[2]. https://kubernetes.io/zh/docs/tasks/configure-pod-container/assign-cpu-resource/
[3]. https://www.cnblogs.com/zhanglianghhh/p/14259632.html
[4]. https://blog.csdn.net/mahui_1980/article/details/115308226?utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromBaidu%7Edefault-5.no_search_link&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromBaidu%7Edefault-5.no_search_link
[5]. https://www.cnblogs.com/Wshile/p/12945909.html
[6]. https://blog.csdn.net/qq_31136839/article/details/95622628
[7]. https://www.cnblogs.com/51core/articles/15104579.html
[8]. https://blog.51cto.com/phospherus/2445758?ivk_sa=1024320u
[9]. https://blog.51cto.com/u_15315026/3200036
[10]. https://blog.51cto.com/u_13760351/2622839
[11]. https://blog.51cto.com/u_15127504/4026704
[12]. https://kubernetes.io/zh/docs/concepts/overview/working-with-objects/namespaces/