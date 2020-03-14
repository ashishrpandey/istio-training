
## Download Istio

    curl -L https://istio.io/downloadIstio | sh -
    cd istio-1.5.0
    export PATH=$PWD/bin:$PATH


## set Istio Profile
    
     istioctl profile dump >default-profile.txt
     istioctl manifest apply --set profile=demo
     istioctl profile dump >demo-profile.txt
     vim -d default-profile.txt demo-profile.txt

