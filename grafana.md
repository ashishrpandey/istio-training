
- When Istio runs with "Demo" profile, it is enabled to run with Grafana.
- If you are running with Default profile, make sure you enable Grafana in the Istio-Operator yaml file.
- Get the list of all services running in istio-system name space

        kubectl get svc -n istio-system 
    
- Edit grafana service to make its type NodePort
- Find out the randomly assigned NodePort of grafana service

- Open in Borwser the following address 

        http://public-ip:NodePort/
        
        


