# System Hardening :

## Section Introduction :

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/c2308661-c578-4fc9-8b77-ca32a5e6545a)

</br>

## Chatper 1 : Least Privilege Principle :

</br>

- Principle of least privilege :

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/6f9ee145-dff0-4111-a889-e5dcf678fa87)

## Chatper 2 : Minimize host OS footprint Intro :

</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/a2c3c7f2-7e19-4e76-9ac4-9078fae685aa)

</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/bf5c3809-587c-4f8a-9b41-3939fd689645)

</br>

## Chatper 3 : Limit Node Access :
</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/53a37e5f-192d-42b3-8ef8-76114f4c6194)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/d1e0f7f1-074f-4874-aa91-3217f3cba793)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/a9e5f77e-d152-47bb-9e30-4652b958b3aa)

</br>

### Types of user accounts in Linux Node.
</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/71908d41-1426-412a-bce3-13ef891027a5)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/d12f59ea-b518-4e41-ac7d-1518f5e97055)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/f5515e92-d723-4c59-8344-25c12e84c6d4)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/51b0f125-b669-4cf9-b347-d105725ba3ec)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/002a77eb-a06c-4a8b-a241-19eb48ee2432)



## Chatper 4 : SSH Hardening :
</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/297be991-ccab-4200-9b84-432cb05825c6)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/741d4c8e-53ba-46b3-9231-897433f4247b)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/e17042c2-0428-4488-88b1-987c5b156f80)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/003d1e70-4616-4cab-b629-2a35d73a790e)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/73ec604f-66f0-43ee-87a1-c2ab808278b6)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/fb86d246-56be-4f73-ba40-27178efafa11)

</br>
</br>

### Reference links </br>
Download the CIS benchmark PDF’s from the below link:

https://www.cisecurity.org/cis-benchmarks/

Go to the `Operating Systems` section and search for the `Distribution Independent Linux`. Expand it to see more options then download CIS Benchmark.

</br>
</br>

### Remove Obsolete Packages and Services
</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/bafef418-44dc-4f25-a7fe-6b2ca492c03c)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/fcab0aca-4fe7-4ced-91d0-ec52a5b4b7fe)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/d7b521bc-8e5e-4630-b37e-071b18c842b7)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/1bc60bee-7b05-4c44-93ed-66d0b36f7ee3)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/ab3fc956-5c89-44b4-b733-e765ac28e858)

### Reference links
</br>

Download the CIS benchmark PDF’s from the below link:

https://www.cisecurity.org/cis-benchmarks/

Go to the `Operating Systems` section and search for the `Distribution Independent Linux`. Expand it to see more options then download CIS Benchmark.


### Restrict Kernel Modules

</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/86287c8e-a051-4d7f-b79f-d91aec60bb9e)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/0dc9eb1a-fbaf-4eaa-b663-c0bf2fc5c622)

</br>
- Unpriviledged process can load the unrequired kernel module by using the network socket, creating a threat.
- This can allow an attacker to exploit the vulnerability.
- Hence we blacklist the kernel module to avoid loading it on the node kernel.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/adc9bb00-d5db-4d73-b5da-1e3eeb875d24)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/419aa648-9490-4b14-a6fd-efd419753363)


### Identify and Disable Open Ports
</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/af2e1513-25bb-4811-8cd7-b589af571ca0)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/4a3aed69-b3b2-4abd-a839-447593b82d9b)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/63c48fe1-d226-4f4a-8d02-94dabdd4a7ba)

</br>
</br>

- Refer to the reference document while installing the software and open the respective port accordingly.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/0a5e5708-fd23-44d8-917b-fdafb2ab050b)

### Reference links 
</br>
</br>
Download the CIS benchmark PDF’s from the below link:

https://www.cisecurity.org/cis-benchmarks/

Go to the `Operating Systems` section and search for the `Distribution Independent Linux`. Expand it to see more options then download CIS Benchmark.

Below are some references:

https://access.redhat.com/security/cve/cve-2019-3874

https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/#check-required-ports


### Minimize IAM roles :
</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/040a4c66-d9c5-4568-932e-86b527382db1)
</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/d969e3de-bf36-4c59-88b0-6165bc77c82f)

</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/e56558bc-89bf-4483-a811-065f886ec614)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/c0bf8f92-f644-4142-81c5-3ab24b8372e5)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/00935951-2a58-4946-a61c-12e7902bfcef)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/4fa9764c-7bc8-4331-a6f1-be62579ad272)

- We cannot attach an IAM policy to the AWS resource, instead we have to create the Role and then assign that role to the AWS resources.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/abb7aa14-d5a2-45e0-922c-5e03a9e8671a)


- Audit the policy and roles and refine them, you can use AWS Trusted Advisor for security checks in realtime and provides the guidance accourdingly.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/8886859e-6ba5-4dfa-90cc-fa429dd17ba8)


### Minimize external access to the network :
</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/999ae430-4745-4d28-aab3-c16ded2a5c67)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/e2aa7d8e-3a38-4439-9188-3d401863d66f)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/194f592a-f4c0-4370-92c8-1c84e1136817)
- OR instead of using these tools you can use linux IPTABLES, UFW tools to apply these policies on the network devices.


### Minimize external access to the network :
</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/15b0fcc7-f959-4003-a988-86237f106b57)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/450ab11e-87bb-4a4c-937d-17c338b18f5b)

</br>
- We can make use of internal packet filtering system in the linux kernel called netfilter. One of the common command line interface to use with the netfilter is IPTABLES. OR you can use the UFW as well.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/c44228ac-3fea-43eb-8480-307ce2f5bc6d)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/133b49d7-5f6e-421c-8dbd-8206a684f92c)

- Install the UFW pacakage.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/8a5fc2e7-b42a-4020-8c45-e898be4f6fb3)

</br>

- Add the UFW Rules.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/c1fd3231-3842-4fe4-8df8-fe90d73d09dd)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/2a9d7fe9-95ee-4f47-82e8-e6c316c52ad4)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/b35cad28-0c6c-4d79-b457-053e0b2cfa47)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/e7cf9eaf-8c8b-4b76-8343-222716386767)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/b619aa85-83e3-4e1a-a1d7-284bf85300e0)








 

 

























































