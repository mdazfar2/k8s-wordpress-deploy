## Deploy WordPress with Kubernetes -

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
     
     I will update you. I have to go to work, but I will update you soon. Thanks for coming. 😊
