# Kubernetes Services

https://kodekloud.com/courses/316262/lectures/4857691



- Services enable communication/connectivity between pods

    - Examples:

       - communication between backend + frontend pods

       - enable frontend app communication to users

       - connectivity to outside data source

       - loose coupling between micro-services


- IPs exist independently on:

    - laptop, but on same network

    - each node

    - container


- `Service`

    - an object


      - Service `Types`:


            - `NodePort service`:

                  - listens to port on node + forwards request on that port to a port on the pod running app

                  - has its own IP address =  `ClusterIp`

                  - `3` ports:

                        - = an array

                        - port on the pod = `80` = `TargetPort`

                        - port on the service = `80`

                        - port on the node = `30008` = `NodePort`

                              - `valid range` =  30000 - 32767


            - `ClusterIp`:


                  - creates virtual IP inside the Cluster


                        - enables communication between different services


                              - EX: set of font end servers to a set of backend servers


            - `LoadBalancer`:


                    - provisions a load balancer for app in supported providers


                            - EX:

                                  - distribute front end load on available servers


    - `Labels` + `Selectors`:


            - enable linking/communication

            - `selectors` in service-definition.yml:


                  - copy labels from pod-definition.yml + place under `selectors`

                  - enables communication between pod and service


## Create Service

        ` kubectl create -f service-definition.yml `

        ` kubectl get service `


        - connect to NodePort via curl or browser:

          - EX:

            ` http://192.168.1.2:30008 `//IP of the node + NodePort



## Multiple Pods

      - all Pods with same label `myapp` communicate w/ service 
