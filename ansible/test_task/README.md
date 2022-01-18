test_task
=========

Installs Docker, Kubelet, runs 2 static pods (prometheus & grafana).


# Files Information
------------------
### Files folder
------------------
>**files/grafana-datasource.yml**  
Config file, adds prometheus as datasource

>**files/grafana-static.yml**  
Pod manifest, runs grafana container  

>**files/kubelet.service**  
Systemd unit file for kubelet service  

>**files/prometheus-static.yml**  
Pod manifest, runs prometheus container  

>**files/prometheus.yml**  
Config for prometheus  

### Tasks folder
------------------
>**tasks/00-install-docker.yml**  
Installs docker and dependencies  
>**tasks/10-install-kubelet.yml**  
Installs kubelet  
>**20-copy-files.yml**  
Copies configs and manifests to host  
>**30-create-static-pods.yml**  
Copies pods manifests  


Run Playbook
----------------
`run.yaml`