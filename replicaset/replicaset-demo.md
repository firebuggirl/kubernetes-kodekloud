https://kodekloud.com/courses/316262/lectures/4857682


## Check yml files via YAML Lint:

    http://www.yamllint.com/

## Create ReplicaSet

    - copy/paste `replicaset-definition.yml` file into Kubernetes master node


    - ` kubectl create -f replicaset-definition.yml `


    - ` kubectl get replicaset `


    - ` kubect describe replicaset `


    - ` kubectl get pods `

## Test ReplicaSet

  - delete one of the pods:

    - ` kubectl get pods `

    - ` kubectl delete pod my-app-replicaset-ztkqn `//or whatever current id is...


          - ReplicaSet will automatically re-create a new pod to replace deleted pod


          - ` kubectl describe replicaset `


    - `kubectl get pods -o -wide `


## Scale up/update

    - set replicas to `6`


    - ` kubectl replace replicaset-definition.yml `

    - ` kubectl get replicast `

    - ` kubectl describe replicaset `

    - ` kubectl get pods `

    -  ` kubectl get pods -o -wide `


## Scale down/update


    - ` kubectl scale --replicas=3 -f replicaset-definition.yml `

    - ` kubectl get replicas `

    - ` kubectl get pods `


        - NOTE: this method does NOT update the `replicaset-definition.yml` file!! This method equates to the imperative approach, which is NOT preferred in Kubernetes.

        - Use the `declarative` approach instead via the `kubectl apply -f` command

    - ` kubectl delete replicaset myapp-replicaset `


    - ` kubectl get all `//list all objects in cluster
