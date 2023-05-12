
## Deploying KEDA with Helm {#helm}

### Install

Deploying KEDA with Helm is very simple:

1. Add Helm repo

    ```sh
    helm repo add kedacore https://kedacore.github.io/charts
    ```

2. Update Helm repo

    ```sh
    helm repo update
    ```

3. Install `keda` Helm chart

    **Helm 3**

    ```sh
    kubectl create namespace keda
    helm install keda kedacore/keda --namespace keda
    ```
Ref:   
https://github.com/kedacore/keda/blob/main/tests/scalers/memory/memory_test.go  
https://keda.sh/docs/2.10/scalers/memory/