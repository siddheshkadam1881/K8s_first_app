Following step required for deploy applications  using Ingress

1) create two application deployment yaml and service  (nginx and apache)

2) create ingress yaml.

3) All service and pods are in same namespace for easy to understand.

4) After this deployment,you need to install ingress nginx  using kind cluster. 
   example:  kubectl apply -f https://kind.sigs.k8s.io/examples/ingress/deploy-ingress-nginx.yaml

5) after check all pods and service after install using following command

        kubectl get pods -n ingress-nginx

NAME                                        READY   STATUS      RESTARTS   AGE
ingress-nginx-admission-create-vz56p        0/1     Completed   0          6h21m
ingress-nginx-admission-patch-kfsxt         0/1     Completed   2          6h21m
ingress-nginx-controller-6b944c4f98-bx262   1/1     Running     0          4h15m

       kubectl get svc -n ingress-nginx

NAME                                 TYPE           CLUSTER-IP     EXTERNAL-IP   PORT(S)                      AGE
ingress-nginx-controller             LoadBalancer   10.96.254.55   <pending>     80:30171/TCP,443:30540/TCP   6h26m
ingress-nginx-controller-admission   ClusterIP      10.96.250.1    <none>        443/TCP                      6h26m

6) controller and service  should be running.

7) use following command for running application in detachment mode:

    nohup kubectl port-forward service/ingress-nginx-controller -n ingress-nginx 8082:80 --address=0.0.0.0 > port-forward.log 2>&1 &

for more details you can use following github URL:

 https://github.com/siddheshkadam1881/K8s_first_app/tree/main/ingress

