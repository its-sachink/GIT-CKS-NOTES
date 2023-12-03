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

</br>
</br>
</br>

## Chapter 5 - Open Policy Agent :
</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/4f8df774-15e9-4834-98b8-d35ac8eb044e)

</br>
</br>


- Authorization : What API can the user access and what actions can they perform, this is taken care by OPA.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/5e6ec3e6-7916-40c2-961f-9ecffd04dc44)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/c5711bcd-c22d-49c4-b3a0-05163019e129)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/703a8d6b-08c0-4314-9085-96d4e2114de8)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/223e679b-7ef0-47fe-b349-137539ac1ed5)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/e11e07ca-4117-44bf-88b8-63c4ef99f25d)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/ea474ec4-335d-4ac9-9619-ae157c05ee39)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/8861a2c2-622c-4cbd-97a5-e478fde2da5b)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/4b6b0ac0-1d1e-47af-97d0-728d69b6dd23)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/ca406f67-7cf6-4959-bb1e-4081036a6926)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/bd4a8c87-b702-44dd-b69f-17d7f0c6b805)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/1d9e9a83-6748-444b-b2b1-7f21e2c1dafc)

#### Reference links
Below are some references:

How Netflix Is Solving Authorization Across Their Cloud [I] – Manish Mehta & Torin Sandall, Netflix

https://www.youtube.com/watch?v=R6tUNpRpdnY

OPA Deep Dive

https://www.youtube.com/watch?v=4mBJSIhs2xQ

</br>
</br>
</br>

## Chapter 6 - OPA in Kuberentes :
</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/f10eabfd-9fc0-449b-b38e-b52d465dec42)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/81f25cdf-f6ca-4f4c-a753-c57fa4e170bd)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/20de1efb-fcd1-4d15-b0fd-7d6c3b83f6e1)


##### Instead of creating our own webhook server and validating the policy.
     - We can connect our mutating or validating webhooks now to OPA.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/a4807787-f68a-4a04-a4e5-46af9672b4fc)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/8d4f64a3-c2de-40dc-a1a6-8e8a5489faee)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/7d7450ca-efaf-406a-9fbb-a9c4fde5b589)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/9bfc7646-5877-4a04-8ca0-9fd9800e6426)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/9bb15b91-eba4-4957-8401-f729ce8049b1)

- Make sure Pods names across all the namespaces are unique.
- Here the information is not send by the validating webhook, as to what all list of Pods are already running in a Cluster.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/02f28613-7993-4fc2-9de5-bfebdbe8c36c)

- How does OPA know about the resources in the kubernetes.
- We can make that happen using a kube-mgmt service.
- KUBE-MGMT Service : It is a service deployed as a side car container along with OPA.
        - It is used to replicate resource definitions from Kubernetes, so they can be cached at OPA.
        - This information can then be imported, and used to refer to objects in the kubernetes while developing policies.
        - It also used to Load policies to OPA, by simply creating a configmap object in kubernetes as a opposed loading policies directly on OPA.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/a789f3a7-5258-4f5f-9108-f3fc1b6026d9)


![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/bb8d2664-71c5-40bb-a4da-9df757048572)

- Earlier we could load policies into OPA by calling policies API using a PUT in CURL operation.
- But now with KUBE-MGMT service, we create a configmap on kubernetes with the label "openpolicyagent.org/policy: rego" and under the data ==>> main section we have the REGO policy defined in a text format.
- The KUBE-MGMT service will identify these policies in a ConfigMap and load them into the OPA as policies. So you don't have to policy to OPA.
- Once KUBE-MGMT service is configured, you have to create the ConfigMap and have the policy defined with in that particular ConfigMap.
</br>
</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/6cec7827-c721-4f3f-8fe0-151c3546ebf1)

- The OPA server and the KUBE-MGMT sidecar container are deployed as a deployment in kubernetes along with the necessary roles and rolebindings for permissions for the KUBE-MGMT service to access the ConfigMaps and a service to make OPA service available to the KUBE-API server.
- All of these is deployed in the OPA namespace.
- For kubernetes to integrate with OPA we create a Validating WebHook configuration.
- All request go through the admission controller through the ValidatingAdmissionWebhook into the OPA service for validation.
- The above method is an older way of integration.
- The newer way is to integrate using the OPA GATEKEEPER Service.




































  




      


      

      








   





  




  










