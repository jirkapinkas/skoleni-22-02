Spustit:

    kubectl apply -f deployment.yml -f service-lb.yml -f ingress.yml

Dále je zapotřebí nastavit DNS. V Linuxu "/etc/hosts", ve Windows "c:\Windows\System32\Drivers\etc\hosts":

127.0.0.1 nginx.example.com

Bude fungovat http://nginx.example.com

Smazání:

    kubectl delete -f deployment.yml -f service-lb.yml -f ingress.yml
