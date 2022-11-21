# CKAD-exam
Preparation and materials for CKAD exam.

### Bookmarks (Chrome)

[CKAD - Chrome Bookmarks](https://github.com/GarfieldZHU/CKAD-exam/blob/main/k8s_chrome_bookmarks.html?raw=true):
- Resources: some online links
- kubernetes: quick guide by kube-resource name
- K8s catalog: catagorized document.

Just import the bookmarks, type the resource name will help you quickly guide to the page.

### Exercises
- [CKAD exercises @dgkanatsios](https://github.com/dgkanatsios/CKAD-exercises)

### Online Material
- [CKAD course @KodeKloud](https://kodekloud.com/courses/certified-kubernetes-application-developer-ckad/)
- [CKAD course with Tests @Udemy (Paid)](https://www.udemy.com/course/certified-kubernetes-application-developer/)

### Kubectl Commands
- [Cheatsheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

### Important sample pages to be used in exam

Offical doc explains the concepts of resources, but it's not what you need in exam. (If you need them in exam, you are really poor prepared.)  

What's really useful is the sampl YAML files for some resources. They are useful. Just find and copy them to your exam will make you easy to pass.

- PV/PVC/Pod use PV

  <details>
    <summary>
    <a href="https://kubernetes.io/docs/tasks/configure-pod-container/configure-persistent-volume-storage/"> sample link </a>
    </summary>
   
    <img width="1004" alt="Screen Shot 2022-11-21 at 4 58 50 PM" src="https://user-images.githubusercontent.com/7751379/203008384-ea754b1a-ea46-435e-ba38-1339cacb2b4e.png">
  </details>

- Network Policy

  [sample link](https://kubernetes.io/docs/tasks/administer-cluster/declare-network-policy/)
  
- etc


### Important alias/variable before exam

```sh
alias k=kubectl                         # will already be pre-configured

export do="--dry-run=client -o yaml"    # k create deploy nginx --image=nginx $do

export now="--grace-period=0 --force"   # k delete pod <pod_name> $now
```

### Vim
- Check your vim config file `~/.vimrc`:
  Add the configs if not to alignment works (exam environment should contain this):
  ```shell
  set nu
  set ts=2
  set expandtab
  set shiftwidth=2
  set autoindent
  ```

- Useful Vim command:
  - `dG` - Deletes contents from cursor to end of file. This is very useful when editing YAML files.
  - `ZZ` - Save and exit quickly.
  - `<n> yy` - Copy n lines from the current line
  - `<n> dd` - Cut n lines from the current line
  - `p` - Paste after this line
  - `P` - Paster before this line
  - `:m,n>` Add one indent line m to n. Use multiple `>`s for multiple indents. 


### Knowledge point

- Network Policy
  [Network Policy Editor for Kubernetes](https://editor.cilium.io/)
  
### Challenges
- [Kubernetes Challenges](https://kodekloud.com/courses/kubernetes-challenges/)
  
### Real Questions
- [CKAD 2021](https://blog.csdn.net/itsaka/article/details/117534764?spm=1001.2014.3001.5502)

---

### Steps to prepare exam

0. Purchase exam
   
   - Couse is not necessary. Or I'll say, it's good, but emmm, not helpful. 
   - In 2022, our company's exchange rate is around 7.0.
   
     If the USD/RMB rate is under 7.0, you can purchase in USD with your Visa/Mastercard.
     
     Otherwise, purchase it on Chinese site with RMB. 🤣


1. Take courses
   Take at least one of the options below as your course should all be good enough:
   a. Purchase the course with CKAD exam as bundle
   
      <img width="426" alt="Screen Shot 2022-11-21 at 5 24 31 PM" src="https://user-images.githubusercontent.com/7751379/203013658-69b71d6c-18b4-404b-8be7-8185911f409e.png">
      
   b. Enroll the KodeKloud course (free trial in 7 days or purchase)
   
      <img width="348" alt="Screen Shot 2022-11-21 at 5 25 09 PM" src="https://user-images.githubusercontent.com/7751379/203013810-231bebed-02d5-41b8-938a-5799debc6c46.png">

   c. Take the course on Udemy. (Same teacher with KodeKloud. Cheaper than paid KodeKloud?)
   
      <img width="331" alt="Screen Shot 2022-11-21 at 5 27 07 PM" src="https://user-images.githubusercontent.com/7751379/203014300-12b3cca9-1988-445c-affb-b66bc25cb94d.png">
      
   d. Just read k8s.io/docs. ***Definitely enough*** if you read all!


2. Practice *important*
   
   CKAD bundled course has no environment. 😥 

   You need to setup your own environment on:
   - GCP/AWS environment: see the course material
   - VRA: [confluence page](https://microstrategy.atlassian.net/wiki/spaces/~645949063/pages/3188818060/Kubernetes+cluster+env+setup+on+CentOS+7)
   
   KodeKloud/Udemy course does. That's helpful. **RECOMMENDED**
   
   PS: Please get used to type `k` instead of `kubectl` during practice. It helps your exam. Absolutely!
   
3. Review
   
   - Quick browse through the Github repo [CKAD exercises](https://github.com/dgkanatsios/CKAD-exercises) to check if you missed some points.
   - Mark down all the official pages with useful YAML sample. (Remember the keyword to search them out)
   - Take more courses if you have enough time.
   - Challenge yourself: https://kodekloud.com/courses/kubernetes-challenges/
   
4. Simulate 

   Your CKAD exam (use your Linux Foundation) gives you 2 chances to simulate on [Kill Shell](https://killer.sh/). Each chance contains:
   - 2-hour test
   - 24-hour environment for reviewing your test results and answers
   
   TIPS:
   a. The simulator is HELPFUL. Take it.
   
   b. The simulator is hard. It's difficult to finish it in 2-hour first time. Just take it easy and try your best.
   
   c. Review and understand each problem and answers after you finish it. No matter how long you take.
   
   d. The second chance is the same question with the first. 
   
    >  You can reserve it the day before you take the real test. And try to finish it as fast as possible. 
    >  
    >  (Just practice your speed.)



### Steps to pass the exam

Once you learned the course and finished the courses, the exam is not hard. I mean it's definitely different to conquer all problems but your goal is passing the exam (66% is good). That's easy with your preparation and ***"Time Management"*** and ***Give Up***


  <details>
    <summary> Sample course page (outdated) </summary>
    <img src="https://user-images.githubusercontent.com/7751379/203023381-7a1f3090-bcab-4066-8ce1-07aef9ab9d3f.png" />
  </details>

1. Open terminal, test `kubectl` and setup shell alias immediately. 
2. Open the browser in Linux remote desktop (not web terminal anymore), navigate to k8s.io/docs. Put your browser and terminal easy to switch.
3. Now begin your problems
4. Read the task, if the task is really long, or it contains some resources you are not familiar (e.g. CRD), just mark it and skip it. 
5. For the task you do not skip, copy the `kubectl config use-context xxx` command and run it immediately. 

   It's important to switch context for each question. 
   
6. Each question has a "task weight", and it actually has sub-tasks. Don't forget the easy sub-tasks. They are your values!

   (e.g. copy your yaml file after you create resources)
   
7. Always use `k` instead of `kubectl`. It saves a lot of time. A 7-character word could be hit typo a lot of times. 🫢 
   - For creating a pod, use `k run`.
   - For creating a simple resource like configmap, secret, use `k create configmap question-10 --from-literal=foo=bar`
   - For creating complicated resources, create YAML file first, then `k apply -f xxx.yaml` or `k create -f xxx.yaml`
   - To create yaml, use the dry-run alias if create yaml template (pod, deployment, etc): 
     `kubectl create deployment --image=nginx question-12 $do`
   - Or copy the yaml template from k8s docs, e.g. pv, pvc, netpol, ingress, egress, etc.
   - Make good use of VIM shortcuts.
     e.g. Turn a job's yaml to a cronjob, use `:m,n>` to indent the job's `template` to `jobTemplate`:
     ```yaml
      apiVersion: batch/v1
      kind: Job
      metadata:
        name: hello
      spec:
        template:
          spec:
            containers:
            - name: hello
              image: busybox:1.28
              imagePullPolicy: IfNotPresent
              command:
              - /bin/sh
              - -c
              - date; echo Hello from the Kubernetes cluster
            restartPolicy: OnFailure
     ```
     - Type `:5,15>>` in command mode. 
     - Insert the cronjob definitions in the line 5:
       ```yaml
          spec:
            schedule: "* * * * *"
            jobTemplate:

     ```yaml
      apiVersion: batch/v1
      kind: CronJob
      metadata:
        name: world
      spec:
        schedule: "* * * * *"
        jobTemplate:
          spec:
            template:
              spec:
                containers:
                - name: hello
                  image: busybox:1.28
                  imagePullPolicy: IfNotPresent
                  command:
                  - /bin/sh
                  - -c
                  - date; echo Hello from the Kubernetes cluster
                restartPolicy: OnFailure
     ```
    - Use VIM command to modify the YAML from sample or dry-run:
      e.g. Create a network policy with 2 egress rules:
      Find the NetworkPolicy sample on [k8s doc](https://kubernetes.io/docs/concepts/services-networking/network-policies/): 
      ```yaml
      apiVersion: networking.k8s.io/v1
      kind: NetworkPolicy
      metadata:
        name: test-network-policy
        namespace: default
      spec:
        podSelector:
          matchLabels:
            role: db
        policyTypes:
          - Ingress
          - Egress
        ingress:
          - from:
              - ipBlock:
                  cidr: 172.17.0.0/16
                  except:
                    - 172.17.1.0/24
              - namespaceSelector:
                  matchLabels:
                    project: myproject
              - podSelector:
                  matchLabels:
                    role: frontend
            ports:
              - protocol: TCP
                port: 6379
        egress:
          - to:
              - ipBlock:
                  cidr: 10.0.0.0/24
            ports:
              - protocol: TCP
                port: 5978

      ```
      - Cut the ingress section off by moving cursor to `ingress` line.
      - Type command `15dd` directly.
      - Move cursor to `to:` line to copy the egress.
      - Type command `6yy`.
      - Move the the end line, type `p`.
      - Finally modify `ipBlock` and `port`. You got this:
      ```yaml
      apiVersion: networking.k8s.io/v1
      kind: NetworkPolicy
      metadata:
        name: test-network-policy
        namespace: default
      spec:
        podSelector:
          matchLabels:
            role: db
        policyTypes:
          - Ingress
          - Egress
        egress:
          - to:
              - ipBlock:
                  cidr: 10.0.0.0/24
            ports:
              - protocol: TCP
              port: 5978
          - to:
              - ipBlock:
                  cidr: 192.168.0.0/16
            ports:
              - protocol: TCP
              port: 8080
 
      ```
