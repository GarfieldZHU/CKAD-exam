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

  [sample link](https://kubernetes.io/docs/tasks/configure-pod-container/configure-persistent-volume-storage/)
  <img width="1004" alt="Screen Shot 2022-11-21 at 4 58 50 PM" src="https://user-images.githubusercontent.com/7751379/203008384-ea754b1a-ea46-435e-ba38-1339cacb2b4e.png">

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


### Steps to 
