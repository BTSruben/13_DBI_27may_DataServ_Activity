# 13_DBI_27may_DataServ_Activity

**Activity Elastic Stack**

**Logstash**

1. Download Logstash 6.0.0

    https://www.elastic.co/downloads/past-releases/logstash-6-0-0

2. Uncompress

    tar xvfz logstash-6.0.0.tar.gz

3. How to execute

    ./logstash-6.0.0/bin/logstash -f <logstash.conf>

Example document:

logstash-conf-example.conf

    05/17/2019,0:00,BROOKLYN,11207,40.673294,-73.89519,GLENMORE AVENUE                 ,NEW JERSEY AVENUE,,0,0,0,0,0,0,0,0,Unspecified,,,,,4133449,Sedan,,,,

Grok tool:

    https://grokdebug.herokuapp.com/

**FileBeat**

1. Download Filebeat 6.0.0

    https://www.elastic.co/downloads/past-releases/filebeat-6-0-0

2. Uncompress

    tar xvfz filebeat-6.0.0-darwin-x86_64.tar.gz

3. How to execute

    ./filebeat-6.0.0-darwin-x86_64/filebeat -e -c <filebeat.yml>

**Elastic**

1. Download Elastic 6.0.0

    https://www.elastic.co/downloads/past-releases/elasticsearch-6-0-0

2. Uncompress

    tar xvfz elasticsearch-6.0.0.tar.gz

3. How to execute

    ./elasticsearch-6.0.0/bin/elasticsearch

**Kibana**

1. Download Kibana 6.0.0

    https://www.elastic.co/downloads/past-releases/kibana-6-0-0

2. Uncompress

    tar xvfz kibana-6.0.0-darwin-x86_64.tar.gz

3. How to execute

    ./kibana-6.0.0-darwin-x86_64/bin/kibana

**Complex Example**

    https://github.com/elastic/examples/tree/master/Common%20Data%20Formats/nginx_logs
    https://github.com/elastic/examples/tree/master/Exploring%20Public%20Datasets/nyc_traffic_accidents
