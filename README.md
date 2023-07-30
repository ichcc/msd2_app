# Votting app (modified)

This repository contains a modified version of the [voting app](https://github.com/dockersamples/example-voting-app), designed to work with Kubernetes Ingress and deployed in its own namespace.

## Deploy

To deploy the modified voting app, follow these steps:

1. Make sure you have `kubectl` configured to connect to your Kubernetes cluster.

2. Create a new namespace for the voting app by running the following command from the current directory:
    ```bash
    kubectl create namespace voting-app
    ```

3. Deploy the application by applying the Kubernetes manifests from the current directory:

    ```bash
    kubectl apply -f ./
    ```

## Check

After deploying the voting app, you can list the existing Ingress resources in the `voting-app` namespace to check if everything is set up correctly:

    ```bash
    kubectl get ingress -n voting-app
    ```

You should see the Ingress endpoints listed, and now you can try to connect to the voting app using these endpoints.

## Destroy

To remove the voting app and all associated resources, run the following command from the current directory:

    ```bash
    kubectl delete -f ./
    ```

This will delete all the resources created in the `voting-app` namespace.

Please note that this modified version of the voting app is intended for use with Kubernetes, and it assumes you have a working Kubernetes cluster where you can deploy the application. If you encounter any issues or have questions, feel free to open an issue in this repository. Happy voting!