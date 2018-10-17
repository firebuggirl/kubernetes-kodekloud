#  Deployments - Update and Rollback


https://kodekloud.com/courses/316262/lectures/4857686



- Rollout:


    ` kubectl rollout status deployment/myapp-deployment `

    ` kubectl rollout history deployment/myapp-deployment `



- 2 Deployment `Strategies`:

    - 1) destroy all instances + re-deploy -> app down = bad

    - 2) take down each instance + replace one by one -> seamless update -> default strategy


- Kubectl Apply:

    - ` kubectl apply -f definition-deployment.yml `//new revision of deployment is created...via declarative approach


    ` kubectl describe deployment myapp-deployment `



- `Upgrades`:


    - ` kubectl get replicsets `//can see that a `new` replicaset has been created


    ....... this enables:

    - ` Rollbacks `//roll back to previous replicaset

          - ` kubectl rollout undo deployment/myapp-deployment `


          -   ` kubectl get replicsets
