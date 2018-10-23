# Service - ClusterIP

https://kodekloud.com/courses/316262/lectures/4857695


- Reminder:

      - can not rely on pod IP addresses. They are mortal.


      - Services solve this problem by creating stable IP(s)


      - `targetPort` = port where backend is exposed

      - `port` = port where service is exposed

      - `selector` = link service to a set of pods


## Create Service

      - ` kubectl create -f cluster-service-definition.yml `

      - ` kubectl get services `
