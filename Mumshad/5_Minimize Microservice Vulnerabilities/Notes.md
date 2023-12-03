## Section Introduction :
</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/4876de1c-a03c-402d-8c5a-81a0d947cb2b)

</br>
</br>
</br>

## Chapter 1 - Security Contexts :
</br>
- You may choose to configure the security setting at the Container level or at a Pod level.
- If configured at a Pod level, the settings will be carried out at the Container level within the Pod.
- If configured at both Pod & Container level, the setting over the Container will override the setting at the Pod level.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/154ba9bb-2eac-4de0-8dea-6c4e0b4c38c4)

- To set the user id at the Container level, move the whole section at the Container level.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/0773ea4f-dc76-48d4-ada1-4fc6d512b555)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/52f76ed1-f049-467a-9a3e-6a1dcff7ebd5)

</br>
</br>
</br>

## Chapter 2 - Admission Controllers :
</br>
![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/37d50bbe-4172-41cc-8a71-d30cd4a6dcf0)

</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/bfafb2aa-a63e-4df5-800e-2cca8fcb0d2a)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/a4f88cb1-ab27-4006-81e1-fbf7e6fb05c8)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/70f9b647-aa44-4ce0-a181-38f5cbe0aa2e)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/c9519c80-e06d-43f7-b819-0360403be4e7)


![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/bf0610ad-9fa8-4042-a8d8-d592dbc35d3e)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/1e129438-1185-45bc-8c8f-3472f534b85b)

- What user is allowed to access what kind of API operation, but what if you want to do more than to define what kind of access user have to the resources.
- For example : When a pod creation request comes in, review the configuration file and look at the image name and
      - Say you do not want to allow deployment of image from public dockerhub image registry.
      - Only allow image from a specific internal registry
      - Use only specific tag for the image
      - If the container is using a root user then do not want to allow that request.
      - Allow certain capabilities only
      - Enforce the metadata always contains labels.

- The above things cannot be achieved using the Authorization or RBAC, that is where you need "Admission Controllers".
      - It helps us implement better security measures, to enforce how a cluster is used.
      - Apart from simple validating the request, it can also change the request or perform additional operation before the pod gets created. 


![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/df115520-a831-4fca-b29f-a4cb63ee4469)

</br>
- There are number of admission controllers that comes prebuild with the kubernetes cluster.
      - AlwaysPullimages
      - DefaultStorageClass
      - EventRateLimit
      - NamespaceExists



![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/4ce5b3c6-cf47-4df8-a91c-16816b303c4e)

</br>
</br>

- Say we want to create a Pod into a namespace "blue" that doesn't exists.
- "NamespaceExists" admission controller check if the namespace exists, if it doesn't exists then it stop the pod from starting up. It is build in admission controller and is enabled by default.
- "NamespaceAutoProvision" is not enabled by default, but it will create the name space if it doesn't exists before starting the Pod.


![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/83847920-e3ea-4d35-836a-2179ef9eafe5)

### Check the default enabled admission controllers.

- To check the default admission controllers that are enabled by default, run below command.


![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/b45c21e6-45f2-4684-b855-9eee3c97c9b9)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/d0248d65-1dab-46df-b75a-59e8b28bbffc)

</br>
</br>
- To Enable the Admission Controller, add the respective flag in the "enable-admission-plugins" section.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/5616bb42-4b9d-4058-af19-df515608fa92)
</br>
</br>
- To Disable the Admission Controller, add the respective flag in the "disable admission plugins" section.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/524f1c34-f5ec-448c-869c-11d176f16004)

</br>
</br>
- Once updated, next time we run the command to provision the Pod in the namespace that does not exists yet, the request goes through
        - Authentication
        - Authorization
        - NamespaceAutoProvision Controller


  ![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/29d201b4-0934-4718-9163-f23958342920)

- "NamespaceAutoProvision" & "NamespaceExists" are now deprecated and is not replaced by "NamespaceLifeCycle".

  ![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/2bfd97e6-7dfc-4812-b320-457b3e216658)
  ![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/ff35dd38-3124-43a0-8265-fa95cb9f3295)

</br>
</br>
</br>

## Chapter 4 - Validating and Mutating Admission Controllers :
</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/2814a897-43bf-4277-bbb4-70f63bf8609a)

</br>
- We will look into different types of admission controllers & how we can configure our own admission controllers.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/af17809f-e8e5-4361-974d-e2a5c441a72e)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/1266839d-437e-4752-932c-d99c1b998c30)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/7b07c763-38e1-448d-b832-3a2a7b254ce1)

</br>
- So, there are 2 types of addmission controllers till now we are seen.
- Mutating Admission Controllers : Are those who change the Object.
- Validating Admission Controllers : Are those who validate the Object definition.
      - There can be a admission controller can also do both, that is mutate & Validate at the same time.
      - Generally mutating admission controller are invoked first by a validating admission controller. So that any change made by mutating one can be validated be considered during the validating process.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/8799e029-1e1b-4650-bfdf-019bd9d8765b)


- What if we want our own Admission controller with our own mutation & validations that has our own logic.
        - 2 support external admission controllers, there are 2 admission controllers available.
              1) MutatingAdmission Webhook
              2) ValidatingAdmission Webhook

  ![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/4785d21a-d959-45aa-9eb4-93f5e09d143f)
</br>
</br>
#### Admission controller webhook :
</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/ea6bb148-c4ff-44b6-ba76-7fc23733c452)


  - We can configure these webhooks to point to a server that is hosted either within the kubernetes cluster or outside it.
          - And our server will have our own admission webhook service running with our own code & logic.
          - After a request is made for the resource, our built in admission controller hits the webhook that is configured.
          - Once it hits a webhook, it makes a call to the admission webhook server by passing in Admission review object in a JSON format.
          - Admission review JSON object : This object has all the details about the request such as
                - the user that has made the request &
                - the type of operation the user is trying to perform
                - on what object & the details about the object itself

          - On receving the request details the Admission webhook server responds with an admission review object with a result of whether the request is allowed or not.
          - If the allowed field in the response it set to true, then the request is allowed or else it is rejected.

</br>
</br>
![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/3cc74069-834b-4358-ac98-3ad397c552d9)


      - So how do we set this up.
            1) First we must deploy a admission webhook server.
            2) Then we configure a webhook on kubernetes, by creating the webhook configuration object.
 
</br>
</br>

#### Deploy a webhook server :

</br>
      ![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/242c8d48-1a9d-4012-9373-6d6607b42c61)

      - Generally written on GoLang language.
      - It must accept the mutate & validate API's and respond in the JSON object that the webserver expects.
</br>
</br>
      ![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/9a6863f8-ef87-4b02-978f-4db4836688ee)

      ![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/d863de0f-cf52-46f5-8c1b-dab0a62395e2)

</br>
</br>
      ![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/122131d7-32d5-48a2-a34e-812b2657ebdc)

      - Once we have developed the webhook server, next step is to host it.
      - So we either run it as a server/containerise it within the kubernetes cluster itself as a deployment.
      - If deployed as a deployment in the kubernetes cluster, then it needs a SVC to be accessed.
</br>
</br>
      ![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/2de7a935-ab17-4425-9549-53183e8f14eb)
</br>
      
      ![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/8146c8a5-29cb-4d91-850b-8085710ee559)

      - The next step it to configure our cluster to reach out to the service to validate or mutate the requests.
      - For this we create a validating configuration object.


      


      

      








   





  




  










