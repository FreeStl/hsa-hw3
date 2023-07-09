Architecture:
Jmeter makes Http POST requests (1000 threads) -> ngix -> app -> mongoDb, elasticsearch.
Metrics:
telegraf reads metrics from ngix, mongoDb, elasticsearch. app sends metrics to telegraf.
telegraf saves metrics to influxdb.
grafana reads and shows metrics from influxdb

screenshots of metrics under load are in the folder grafana/screenshots

How to run:
run docker-compose

send request to nginx: POST http://localhost:80/api?id=1&name=maxim , where id - any id of person; name - any name of person.


