Spustit:

    kubectl apply -f service-external.yml -f endpoint-external.yml
    kubectl run curl-nginx --image=radial/busyboxplus:curl -i --tty --rm
    curl http://external-seico

Měla by se získat nějaká odpověď ze serveru. Pokud nefunguje, pak je zapotřebí změnit IP adresu serveru (v endpoint-external.yml).

Smazání:

    kubectl delete -f service-external.yml -f endpoint-external.yml
