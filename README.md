# Deploy WordPress with Kubernetes -

Firstly we use Kustomization file in Kubernetes are used to declare **resources and customizations**. The kustomization.yaml file is a specification of resources plus customizations, and it is used to declare the manifests you want to change and how you want to change them.

- **In the above repo, you will find the YAML code for kustomization, and within the kustomization, there are two more YAML files called 'mysql-wordpress.yml' and 'wordpress-deployment.yml'.**

## when you are add both of the code with repective yaml file name then run the below commands step by step -

1. **To create the kustomization file, you have to use this command**👇

    ```bash
    kubectl create -k .
   ```

    - This command will automatically check whether the kustomization file is available or not. If it is available, the kustomization file will be run automatically.

2. **After creating the kustomization file, many more clusters are run because we are adding too many clusters in the kustomization. So, if you want to check them all, use the commands step by step.**

   ```bash
   kubectl get svc
   ```

    - It will show the services is created or note if created then all good.
  
  3. **To check the deploy**

     ```bash
     kubectl get deploy
     ```

      - There two deploy will shown called "wordpress" & "wordpress-mysql"
    
  4. **To check the replicaSet**

     ```bash
     kubectl get rs
     ```

      - Also, two ReplicaSets will be shown, but you have to wait until the status of all the ReplicaSets becomes 'run.
    
  5. **To check the pods**

     ```bash
     kubectl get pods
     ```

     - When the status of the replicaSet is ready then you have to get two pods when the pods is also ready then you are good to go..
    
  6. **To check the Secrets**
     
     ```bash
     kubectl get secret
     ```

     - It allows you to retrieve information about a secret. By default, the command does not display the contents of a secret. This is to protect the secret from being exposed accidentally or from being 
       stored in a terminal log

7. **To check PersistentVolumeClaim**

   ```bash
   kubectl get pvc
   ```
   - It is a request for a specific amount of storage from a persistent volume and when it is available then it you get PersistentVolume.

8. **To check PersistentVolume**

   ```bash
   kubectl get pv
   ```
   -  It is a piece of storage in a Kubernetes cluster that is provisioned and managed by the cluster’s administrator. It is a way to separate storage from the actual pod that needs it.

9. **To get port using services**

    ```bash
    kubectl get svc
    ```
    - You will get wordpress and wordpress-mysql remember that you have to use port of the wordpress when you will get it on.
  
10. **It's time to deploy your wordpress using ip**

    ```bash
    minikube ip
    ```
    - After using this command, you will get the IP address. Once you get the IP, use the same IP in your browser, attaching the port which you will get from the 'svc' command.
   
- Now, congratulations! ✨ You have completed deploying your WordPress. Enjoy your WordPress journey! 😊

  ***If you are facing any issues then feel free to message me on - [LinkedIn](www.linkedin.com/in/md-azfar-alam) or [Discord](https://discordapp.com/users/877531143610708028)***

