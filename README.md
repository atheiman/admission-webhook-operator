# Admission Webhook Operator

Kubernetes mutating and validating admission webhooks are very powerful and a huge improvement over existing admission controllers that must be enabled in the api-server at startup. Read more here: https://kubernetes.io/docs/reference/access-authn-authz/extensible-admission-controllers/

Unfortunately, creating a simple admission webhook is a bit more work than it should be right now. This operator is an attempt to make it easier to run an admission webhook by only deploying a single custom resource definition.

## Local Dev

Notes from getting started (also see [Operator framework - Helm user guide](https://github.com/operator-framework/operator-sdk/blob/master/doc/helm/user-guide.md))

```
sudo ln -s $PWD/helm-charts/admissionwebhook /opt/helm/helm-charts/
kubectl apply -f deploy/crds/admissionwebhook_*_crd.yaml
operator-sdk up local
```
