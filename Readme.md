


Após instalar o astro sdk

acesse a pasta em que o projeto foi clonado

astro dev init 

astro dev start

http://localhost:8080/home

user: admin
password: admin

docker build spark/master -t airflow-spark-master
docker build spark/worker -t airflow-spark-worker

astro dev bash

airflow tasks test stock_market is_api_available 20240720
airflow tasks test stock_market get_stock_prices 20240720

docker build spark/notebooks/stock_transform -t airflow/stock-app