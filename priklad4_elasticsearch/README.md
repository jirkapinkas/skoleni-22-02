# Spusteni:

    kubectl apply -f elasticsearch.yml
    kubectl apply -f kibana.yml

# Jak ziskat heslo (Linux):

    kubectl get secrets quickstart-es-elastic-user -o go-template='{{.data.elastic | base64decode}}'

# NEBO (Windows) ... vrati heslo ve formatu Base 64, ktere je nutne nasledne dekodovat do plaintextu:

    kubectl get secrets quickstart-es-elastic-user -o json

# Elasticsearch (HTTPS!!!):

https://localhost:9200

# Kibana (HTTPS!!!):

https://localhost:5601

# Username: elastic

# Smazani:

    kubectl delete -f elasticsearch.yml
    kubectl delete -f kibana.yml
