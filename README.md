# [zeeqs-helm](https://github.com/livspaceeng/zeeqs-helm)

Helm chart to host [ZeeQS](https://github.com/zeebe-io/zeeqs) app on Kubernetes cluster
> **Latest Chart version: 1.0.0**

### Deployment Steps
- Clone these 2 repo in your home (**~**) directory:
  + [zeeqs helm repo](https://github.com/livspaceeng/zeeqs-helm)
  + [helm-chart repo](https://github.com/livspaceeng/helm-charts)
- Make any required changes to [zeeqs-helm](https://github.com/livspaceeng/zeeqs-helm) repo.
- Update the **appVersion** in [Chart.yaml](./zeeqs/Chart.yaml) to point to the current [zeeqs version](https://github.com/zeebe-io/zeeqs/releases) (*Just to be aware of the current version being used*).
- Upgrade the **version** in [Chart.yaml](./zeeqs/Chart.yaml), and push to this repo.
- Run the below commands from terminal (*inside ~/helm-charts directory*):
  + `> helm package ../zeeqs-helm/zeeqs`
  + `> helm repo index --merge index.yaml --url https://charts.livspace.com .`
  + `> git commit`
  + `> git push origin`
- Use the **version** from [Chart.yaml](./zeeqs/Chart.yaml) and update it in [requirements.yaml](https://bitbucket.org/livspaceeng/environment-jx-dev/src/master/env/requirements.yaml).

That's it! ;)
