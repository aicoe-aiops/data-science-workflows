# Troubleshooting JupyterHub for Data Scientists

Data scientists using Jupyterhub may encounter problems while running their workloads. This document highlights how to troubleshoot some common problems. If you get an error that is not explained in this document, make sure to create an issue in the [support repository](https://github.com/operate-first/support) for the Operate First project. 


# Resource usage


## RAM

A lot of the common problems are related to the memory consumption of the workload. If your notebook requires more RAM than what is requested by your instance, you will likely see your kernel crash. In this case, you can look at your memory consumption chart:



*   If you are using an Elyra image, you can see a sum of memory used by all your active kernels at the bottom of your screen.

![Elyra notebook RAM](./../public/assets/troubleshooting_jh/elyra_memory.png)

*   You could also go to the [Grafana dashboard](https://grafana-route-opf-monitoring.apps.zero.massopen.cloud/d/YuYfkHYMk/jupyterhub-usage?orgId=1&var-user_id=shanand-40redhat-2ecom) and select your username to see the resource usage for your pod.
*   Currently, you can spawn a pod with memory ranging from 1GB to 32GB.


## PVC

You could also run into problems spawning your pods and this could be because your PVC is full. If you are not able to spawn your pod, check the PVC status in the [grafana dashboard ](https://grafana-route-opf-monitoring.apps.zero.massopen.cloud/d/YuYfkHYMk/jupyterhub-usage)and if it is full, request for more space on the support repository for Operate First. You  can also find this information in your Jupyterhub terminal by using the following command:

df -h /opt/app-root/src 


## CPU

To monitor the real time CPU and GPU resources used by your data science workload, check the [grafana dashboard](https://grafana-route-opf-monitoring.apps.zero.massopen.cloud/d/YuYfkHYMk/jupyterhub-usage) for spikes and falls. 

If you can not understand the issues that you are experiencing, you could check the [pod logs](https://console-openshift-console.apps.zero.massopen.cloud/k8s/ns/opf-jupyterhub/pods) for your instance. If you do not have access to the logs, reach out to the support repository or the slack channel.


# Resources



*   [Grafana dashboard](https://grafana-route-opf-monitoring.apps.zero.massopen.cloud/d/YuYfkHYMk/jupyterhub-usage) for monitoring resource usage
*   [Pod logs](https://console-openshift-console.apps.zero.massopen.cloud/k8s/ns/opf-jupyterhub/pods) for detailed errors
*   [Support repository](https://github.com/operate-first/support) for unknown errors
*   [Slack channel](https://join.slack.com/t/operatefirst/shared_invite/zt-o2gn4wn8-O39g7sthTAuPCvaCNRnLww) for communication