Spustit:

    kubectl apply -f deployment.yml -f service-lb.yml
    kubectl run curl-nginx --image=radial/busyboxplus:curl -i --tty --rm
    curl http://nginx:8080

Pokud je v service-lb.yml typ service ClusterIP, pak bude pouze fungovat curl z jiného podu. Pokud je typ LoadBalancer, pak bude také fungovat http://localhost:8080 (s Docker Desktop)

Měla by se získat nějaká odpověď ze serveru.


Smazání:

    kubectl delete -f deployment.yml -f service-lb.yml