```sh
ps aux | grep elasticsearch
```

```sh
curl localhost:9200/_nodes/stats/process?pretty
```

To restart elasticsearch, it is recommended to kill the process then start again.
/var/run/elasticsearch/elasticsearch.pid

```sh
sudo kill <pid>
sudo /etc/init.d/elasticsearch start
```

http://www.oodlestechnologies.com/blogs/How-to-solve-No-Access-Control-Allow-Origin-with-elastic-search
