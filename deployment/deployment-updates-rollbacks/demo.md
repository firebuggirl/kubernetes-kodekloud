
# Upgrade Demo

https://kodekloud.com/courses/316262/lectures/4857687

    ` kubectl get all `//check for running deployments


    ` kubectl create -f deployment-definition.yml `

    ` kubectl rollout status deployment-definition.yml `

    ` kubectl rollout history deployment-definition.yml `

    ` kubectl rollout history deployment-definition.yml `

    ` kubectl delete deployment myapp-deployment `

    ` kubectl get all `


- start over + get Kubernetes to record the change:


      ` kubectl create -f deployment-definition.yml --record `

      ` kubectl rollout status deployment-definition.yml `

      ` kubectl rollout history deployment-definition.yml `//now can see the change-cause

- change `nginx` image in yml file to a different version...ie., : ` nginx:1.12`...check Docker Hub for image versions


- Apply change:


      `  kubectl apply -f deployment-definition.yml  `

      ` kubectl rollout status deployment/myapp-deployment `

      ` kubectl get deployment `

      ` kubectl get pods `

      ` kubectl describe deployment `

      ` kubectl rollout history deployment/myapp-deployment `

- Alternative/non-declarative approach (not recommended):

      ` kubectl set image deployment/myapp-deployment nginx-container=nginx:1.12-perl `//another version yet still...

      ` kubectl rollout status deployment/myapp-deployment `


      ` kubectl rollout history deployment/myapp-deployment `

      ` kubectl describe deployments `

      - roll back last change/version if/when a bug occurs in app:

           ` kubectl rollout undo deployment/myapp-deployment `

           ` kubectl rollout history deployment/myapp-deployment `

           ` kubectl describe deployments `


     
