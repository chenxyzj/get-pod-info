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
