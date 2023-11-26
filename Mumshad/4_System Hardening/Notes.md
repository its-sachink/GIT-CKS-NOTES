![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/592c27af-be31-48ed-9877-d040b0ddb4fa)# System Hardening :

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

</br>
</br>
</br>

### Linux Syscalls :
</br>

- We will understand the Linux system calls and what happens when a application runs under a hood.

- Kernel is the interface between Hardware and Application.

- Kernel runs inside the Kernel space which include the kernel code, kernel extensions and the device drivers.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/fbfa5683-ce88-4202-b726-f960e0429743)

- Applications running on user space get access to data on devices by making special request to the kernel called systems calls.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/31d02878-f4bc-4dbe-bbf0-d5246e4d1e83)

- For example to create an empty file to create the error.log file it will execute several system calls.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/2cf8fde2-4696-41fb-96bf-e8b4eeb1f66e)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/6411ba4f-12d5-4e9e-bac0-ee2dbb0a2988)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/39afe969-981c-4d21-abb8-740f9b77810c)


- To trace the syscalls invoked by the running process, you need to find the PID of the running process.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/e0aefa89-556d-43fa-992c-29e407d28ccb)

- Summary of all the syscalls used by the command.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/75a06372-d336-43c0-b606-a5bedfb90778)


</br>
</br>
</br>

### AquaSec Tracee :
</br>

- Tracee : A tool from aquasec which can be used to trace a syscall on a containers.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/27d15746-e7c4-4291-812a-39b0274b7320)

- It uses eBPF to trace the system calls, eBFP can run the programs directly on the kernel space without interfering in the kernel source code or without loading any kernel modules.
- As a result eBPF programs are used to create tools, that can monitor the OS and detect suspicious behavior.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/903faa7a-03a8-49c7-a120-29797065c303)

- Tracee uses an eBPF technology and is run as a docker container and build & run the program in /tmp/tracee directory by default.
- Bind mount the directory from the host to the containers.
- Tracee also needs an access to kernel modules in /lib/modules & /usr/src.
- Finally tracee needs priviledged access as well on the host.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/afa49427-d6bd-4901-a4ec-b213c1cb7e77)


- Way to capture the syscall from the containers.

- To observe the syscall generated from the single command such as `ls` from the container, run with below options.
-  -- trace comm=ls

 ![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/a979f8ae-32b2-4959-882d-6eb676bd32bf)

 - Similarly to observe all the syscall from the process of the container run the below command.
 -  --trace pid=new
 -  This will give output for all the new processes generated on the hosts.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/21919a1b-354c-4855-a0fd-c4ca8426319b)


- Observe syscalls generated from the new container. Run with the flag,
-  --trace container=new

  ![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/a6841dfa-5f9c-40e5-acc8-fd7a5a9bc2e8)

</br>
</br>
</br>
 
  
### Restrict syscalls using seccomp :
</br>

- We will see how to allow programs to only make syscalls that they absolutely need.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/3b9e5625-a36e-45d9-bff7-b99ec1916c7b)

- Currently there 435 syscalls in linux, all of them can be used by application running in user space, however not all application require access to these many syscals.
- 
![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/b99a3d98-a7bf-4d8d-b741-26919f4668a3)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/154a8fbe-c3c3-42db-93eb-c7014445c64d)

</br>
</br>

- How do we restrict applications running on Host/container to only use syscalls that they need access to actually perform there jobs.
- By default all syscalls invoke is allowed, increasing the attack surface.

</br>
- This is where we can use SecComp : Secure computing, it is a linux kernel level feature that can be used to sandbox applications to only use the syscalls that they actually need.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/971cd493-a9f3-4d7c-8895-8d6fe7ecfa5a)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/e0c02a98-291c-4575-9bb3-883270bdae36)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/86d0b5b7-9804-4d21-a012-bd86aa98a9fb)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/6120e947-e6a8-4092-8e88-218b8f21645d)

- Docker has a build-in seccomp filter that it uses by default whenever we create a container, provided that the host kernel is SecComp enabled.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/c680effd-b013-4641-be08-dc17e47d3b50)

- White list profile SecComp :White list selective SecComp and block are the remaining.
- 
![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/4ba98219-1b9c-4239-ac8e-e3e542ee19d9)

</br>
- Black list profile SecComp : allow every syscall and reject the selective syscalls. They are easier to create.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/efa3f849-f765-473a-8642-f79457f32662)

</br>

- Default Docker SecComp profile blocks around 60 of the 300 syscalls on the x86 architecture.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/8586c97a-92bd-4e86-a1c5-dce8136f2814)

</br>
- Use the Custom SecComp profile.
![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/b479458c-44ca-4f8e-8a5d-84e39bda200b)

</br>
- Disable using SecComp completely by using `--security-opt seccomp=unconfined`

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/ca725f93-48c4-4de6-ad0f-91b43709298c)

</br>
</br>
</br>
### Implement Seccomp in Kubernetes :
</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/c0b75ce1-0979-46fb-b234-eddf8d57251f)

</br>
- Docker blocks around 60 SysCalls calls in there default SecComp profile. You can test this by running a simple tool "amicontained".

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/e5a381e6-bbe8-4cf5-983d-3d1e9aaf1774)

</br>
- Now lets run the same image in the kubernetes Pod.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/5839548c-e4ea-4eb3-9751-f1fdc05183da)

- Kubernetes does not use the SecComp profile by default

</br>

- How to implement/apply SecComp in the Kubernetes environment.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/8b5757de-6d89-4038-a5e0-ae97f455666d)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/919e8d6c-0f2b-4180-8210-0ca14bbc9ef0)


- How to apply custom SecComp profile.
- The profile file should be under /var/lib/kubelet/seccomp/profiles directory
![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/d5763b65-a078-4c52-8190-c764de34b442)

</br>

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/df73fc94-bd49-4f25-b424-343673ec381a)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/992cfde4-e3e0-43f0-9fc9-8c80ea59d775)

</br>
- How to map the syscall number to the action it is performing.
- Check the mapping in the directory "/usr/include/asm/uninstd_64.h

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/10d155a9-eccb-40cf-a1b2-77c2e745d1c0)

</br>
- We can also make use of the tracee tools to analyse the syscalls made by the containers.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/9dfa1891-8b34-465d-a10e-d373aeb2f375)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/27b05ca1-afee-48f1-8214-952f51ebfcee)

</br>
- Profile to reject all syscalls made by the containers. Set the default action to SCMP_ACT_ERRNO.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/ae474150-eb21-488c-9e23-d50798fb0ae7)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/3738b812-44e5-44fd-820d-805a9a198f16)

</br>
- To make use of the custom profile, place the JSON file inside the same directory. This custom profile file can be created after testing what all syscalls
our application makes.

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/3d93527d-a008-4b33-a391-e9445f50678d)

![image](https://github.com/its-sachink/GIT-CKS-NOTES/assets/25415707/871f9213-6aac-406c-b3ae-160bb579c7a7)

</br>
- Exam Tip : They might not ask to create a custom SecComp profile, however they will ask to copy the custom SecComp profile to the default SecComp location to the all nodes of the kubernetes cluster.
- An then use it to create the Pods.














































  














 

 

























































