---
hide:
  - toc
---

# Multicloud Services

Multicloud services are applications running on a group of Pods, which are exposed as network services one by one.
Using the DCE multicloud orchestration module, you can use unfamiliar service discovery mechanisms without modifying your applications.
DCE provides the IP address for the Pod running the service and provides the same DNS name for a group of Pods, which can be load balanced among these Pods.

Follow the steps below to manage multicloud services.

1. After entering a multicloud instance, in the left navigation bar, click `Resource Management` -> `Multicloud Service`, and click the `Create Service` button in the upper right corner.

    ![Create](../images/service01.png)

2. On the `Create Multicloud Service` page, after configuring the access type, deployment location, port configuration and other information, click `OK`. The deployment location is divided into four methods: selecting from multicloud workloads/designating clusters/designating regions/designating labels. For the latter three methods, please refer to the detailed introduction in Workloads. Here, select from workloads is added, that is, inherit the selected workloads. Deployment policy (pp) in .

    ![Deploy](../images/service02.png)

3. It supports one-click conversion of sub-cluster services to multicloud services. Click `Convert Now` on the list page, select the service under the specified working cluster and namespace, and click OK.

    ![Convert](../images/service03.png)

4. Check the multicloud service list at this time, and find that the sub-cluster service has been upgraded successfully.

    ![Upgrade](../images/service04.png)

5. Click `⋮` on the right side of the list to update and delete the service.

    ![Update/Delete](../images/service05.png)

    !!! note

        If a service is deleted, the information related to the service will also disappear, please operate with caution.

## YAML example

Here is an example YAML for a multicloud service that you can use with a little modification.

```yaml
kind: Service
apiVersion: v1
metadata:
  name: kubernetes
  namespace: default
  uid: a23a0616-789e-469f-88f5-07eb67d460dc
  resourceVersion: '190'
  creationTimestamp: '2023-04-13T10:11:19Z'
  labels:
    component: apiserver
    provider: kubernetes
  annotations:
    shadow.clusterpedia.io/cluster-name: k-kairship-jxy
spec:
  ports:
    - name: https
      protocol: TCP
      port: 443
      targetPort: 5443
  clusterIP: 10.96.0.1
  clusterIPs:
    - 10.96.0.1
  type: ClusterIP
  sessionAffinity: None
  ipFamilies:
    - IPv4
  ipFamilyPolicy: SingleStack
  internalTrafficPolicy: Cluster
status:
  loadBalancer: {}
```
