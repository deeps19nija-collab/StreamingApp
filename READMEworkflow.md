Created the ECR repository

![alt text](image.png)

Build the dockerfile for each service like admin-service  

![alt text](image-2.png)

Now, login to Docker using ECR repo  
![alt text](image-3.png)  

After login succedded, tag and push the docker image created locally to ecr repository.

![alt text](image-4.png)

![alt text](image-5.png)

Do the same steps for rest of the services and push the images to ECR repos 

![alt text](image-6.png)

![alt text](image-7.png)

![alt text](image-8.png)

![alt text](image-9.png)  

**Create EKS cluster**

<img width="1417" height="300" alt="image" src="https://github.com/user-attachments/assets/67538440-42c3-4ce5-8430-cdb4abd997e4" />

<img width="1796" height="913" alt="image" src="https://github.com/user-attachments/assets/22e93fdb-e599-4135-b165-01f647942519" />  

**Create the private S3 bucket and create the cdn cloudfront to allow the operations in bucket**



**Create helm charts**
https://github.com/deeps19nija-collab/StreamingApp/tree/main/helm


**Now to enable eks to pull the images from EKS cluster, we need to add the required policies and roles as below**

1. Create IAM policy to allow ECR repo with pull permissions
   <img width="1638" height="927" alt="image" src="https://github.com/user-attachments/assets/735bea1e-6160-44b0-8dbb-80ccb7d492a0" />

2. Give EKS worker nodes the right IAM permissions to pull the images.

   Step 2 — Attach ECR permissions to the node role

Go to IAM → Roles → <Node Role> → Attach Policies

Attach AmazonEC2ContainerRegistryReadOnly

<img width="1918" height="1040" alt="image" src="https://github.com/user-attachments/assets/81fbcd79-02e5-411b-906f-63af325e41f6" />




















