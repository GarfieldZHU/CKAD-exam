# CKAD-exam
Preparation and materials for CKAD exam.


### Exercises
- [CKAD exercises @dgkanatsios](https://github.com/dgkanatsios/CKAD-exercises)

### Online Material
- [CKAD cource @KodeKloud](https://kodekloud.com/courses/certified-kubernetes-application-developer-ckad/)

### Kubectl Commands
- [Cheatsheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

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
