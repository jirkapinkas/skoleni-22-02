Spuštění (je zapotřebí nainstalovanou mít Javu, Maven & Docker):

cd demo
mvn spring-boot:build-image
cd ..
kubectl apply -f demo.yml -f demo-service.yml

Funguje: http://localhost:8080

Smazání:

kubectl delete -f demo.yml -f demo-service.yml
