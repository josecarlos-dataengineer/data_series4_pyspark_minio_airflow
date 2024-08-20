


Após instalar o astro sdk

acesse a pasta em que o projeto foi clonado

astro dev init 

astro dev start

http://localhost:8080/home

user: admin
password: admin

### connections
connection id: stocks_yahoo
connection type: http
host: https://query1.finance.yahoo.com/

extra: {
"endpoint":"/v8/finance/chart/",  
"headers":{
  "Content-Type":"application/json",
  "User-Agent":"Mozilla/5.0"}
}


### minio

connection_id: minio
connection_type: AWS Web Services
AWS Access Key ID: minio
AWS Secret Access Key: minio123

extra: {"endpoint_url":"http://host.docker.internal:9000"}

localhost:9000

MINIO_ROOT_USER: minio
MINIO_ROOT_PASSWORD: minio123

![alt text](imagens/minio.png)

### Spark
cd spark/notebooks/stock_transform/
docker build . -t airflow/stock-app



docker build spark/master -t airflow-spark-master
docker build spark/worker -t airflow-spark-worker

astro dev bash

airflow tasks test stock_market is_api_available 20240720
airflow tasks test stock_market get_stock_prices 20240720

docker build spark/notebooks/stock_transform -t airflow/stock-app