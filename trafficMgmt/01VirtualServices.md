## Getting started with Destination Rules, Subsets and Vrtual Services

* Virtual service requires Destination Rules 
* DestinationRule defines subsets. 
* Subset creation is done using Labels 

      cd samples/bookinfo/networking
    
Look how to define Destination rules and subsets:

    vim destination-rule-all.yaml
    
Apply Destination Rules ad corresponding subsets

    kubectl apply -f  destination-rule-all.yaml
    
Define the virtual services for every version v1 for every service
- Even though there are 3 versions of review are there it will make sure that all the traffic goes to reviews-v1 

Look at how to define virtual services and their association with Destination Rules - 

    vim virtual-service-all-v1.yaml
    
Create the virtual services 

    kubectl apply -f virtual-service-all-v1.yaml
    
    
Checkout the DestinationRules and virtual services thus created: 

    [root@ip-172-31-19-150 networking]# kubectl get dr
    NAME          HOST          AGE
    details       details       19m
    productpage   productpage   19m
    ratings       ratings       19m
    reviews       reviews       19m


    [root@ip-172-31-19-150 networking]# kubectl get vs
    NAME          GATEWAYS             HOSTS           AGE
    bookinfo      [bookinfo-gateway]   [*]             149m
    details                            [details]       6m37s
    productpage                        [productpage]   6m37s
    ratings                            [ratings]       6m37s
    reviews                            [reviews]       18m





