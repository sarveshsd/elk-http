# elk-http

## This is for deploying elasticsearch and kibana both on http 

 - If u want pv and pvc for elastic-search u will need to add it yourself just provide both file to chatgpt and it will work
 - In Kibana.yaml file u should check the env section to run u'r server in http
      
          env:
          - name: SERVER_NAME
            valueFrom:
              fieldRef:
                fieldPath: metadata.name
          - name: SERVER_HOST
            value: "0.0.0.0"
          - name: ELASTICSEARCH_HOSTS
            value: http://es-service.default.svc.cluster.local:9200

            This section will run your kibana in http
   
