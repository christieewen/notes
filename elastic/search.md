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

To edit the configuration file, 1. Get information about the elasticsearch process with the unix command "ps" and/or peep into the elasticsearch script.
```sh
sudo emacs /etc/init.d/elasticsearch
```
Edit the configuration file.
```sh
sudo emacs /etc/elasticsearch/elasticsearch.yml
```
