# Deployments

https://kodekloud.com/courses/316262/lectures/4857683




  - A `Deployment` is an `object` higher up in the Kubernetes hierarchy

      - can upgrade underlying instances seamlessly

      - Structure =

            - `Deployment`

              - `Replica Set`

                - `Pods`

                  - `Containers`


  - Rolling updates

## Create Deployment Object

  - ` kubectl create -f definition-deployment.yml `

  - ` kubectl get deploy `

  - ` kubectl get replicaset `

  - ` kubectl get pods `

## Get/see all objects

  - ` kubectl get all `

  - ` kubectl describe deployment `


## YAML Lint

    http://www.yamllint.com/
