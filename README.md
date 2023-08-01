# A snap for KPT

This project contains a snap for [kpt](https://github.com/GoogleContainerTools/kpt), a tool for automating Kubernetes Configuration Editing.

## Usage

1. Install the `kptcli` snap

    ```console
    snap install kptcli
    ```

2. Create an alias to run `kpt` directly

    ```console
    sudo snap alias kptcli.kpt kpt
    ```

3. Use `kpt`

    ```console
    kpt pkg get --for-deployment https://github.com/nephio-project/nephio-packages.git/nephio-configsync
    kpt live init nephio-configsync
    kpt live apply nephio-system --reconcile-timeout=15m --output=table --kubeconfig=/home/ubuntu/.kube/config
    ```

> Note: You will need to be specific about the kubeconfig directory.
