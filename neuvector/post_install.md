
## The NewVector external access

### External access
By Default Neuvector will be exposed as a NodePort service and you will be able to find the NodePort using command 
```
NODE_PORT=$(kubectl get --namespace neuvector -o jsonpath="{.spec.ports[0].nodePort}" services neuvector-service-webui)
echo $NODE_PORT
```
Once you have the NodePort, you can access by NODE_IP(you can find from the kubesonfig file or from the Civo UI):NODE_PORT. The default username:password is admin:admin.
```
For more information you can visit the [Newvector Website](https://open-docs.neuvector.com/deploying/kubernetes).
