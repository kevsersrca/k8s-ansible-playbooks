# k8s-ansible-playbooks


add hosts file and run

```
ansible-playbook -i hosts site.yml

PLAY [k8s] **********************************************************************************************************************************

TASK [Gathering Facts] **********************************************************************************************************************
ok: [master]
ok: [node]

TASK [k8s : Update repository and Upgrade packages] *****************************************************************************************
ok: [node]
ok: [master]

TASK [k8s : Install packages that allow apt to be used over HTTPS] **************************************************************************
ok: [node]
ok: [master]

TASK [k8s : Add an apt signing key for Docker] **********************************************************************************************
ok: [node]
ok: [master]

TASK [k8s : Add apt repository for stable version] ******************************************************************************************
ok: [node]
ok: [master]

TASK [k8s : Install docker and its dependecies] *********************************************************************************************
ok: [master]
ok: [node]

TASK [k8s : Remove swapfile from /etc/fstab] ************************************************************************************************
ok: [node] => (item=swap)
ok: [master] => (item=swap)
ok: [node] => (item=none)
ok: [master] => (item=none)

TASK [k8s : Disable swap] *******************************************************************************************************************
ok: [master]
ok: [node]

TASK [k8s : Add an apt signing key for Kubernetes] ******************************************************************************************
ok: [node]
ok: [master]

TASK [k8s : Adding apt repository for Kubernetes] *******************************************************************************************
ok: [master]
ok: [node]

TASK [k8s : Install Kubernetes binaries] ****************************************************************************************************
ok: [node]
ok: [master]

PLAY RECAP **********************************************************************************************************************************
master                     : ok=11   changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
node                       : ok=11   changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   

```
