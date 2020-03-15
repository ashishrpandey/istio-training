
## Problem Statement: 
 - All traffic from a particular user named Jason shall be routed to the service reviews:v2.
 - Rest of the other traffic should be routed to reviews:v1
 
 Apply the rule for Jason User: 
 
    cd  samples/bookinfo/networking/
    kubectl apply -f virtual-service-reviews-test-v2.yaml
    
 Observe the virtual service:
  
    kubectl get virtualservice reviews -o yaml
    
  ## Validate it 
  
  - In the browser open the productpage: 
  - http://<public-ip>:<nodeport>/productpage/
  
   - Login as Jason user
        -  you shall see the page with version v2 (black star)
        
   - Login as any other user
        - you shall see the page with version v1 (No star)
        
        
        
   
  
    
