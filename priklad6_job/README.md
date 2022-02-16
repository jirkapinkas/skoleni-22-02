Spuštění:

    kubectl apply -f job.yml
    kubectl get pods
    kubectl logs NAZEV_PODU
    # Vypíše hodnotu pi s přesností na 2000 desetinných míst
    # Pod zůstane vytvořen (bude ve stavu Completed)

Smazání:

    kubectl delete -f job.yml
