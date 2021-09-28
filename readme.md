# 测试通过Downward API传递pod信息给容器内应用

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
