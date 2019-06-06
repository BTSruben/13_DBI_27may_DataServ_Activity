Create an EC2 Instance

    aws ec2 run-instances --image-id ami-08cb992fa60479feb --count 1 --instance-type m5.xlarge --key-name rubens_paris --security-group-ids sg-0e8cb59d207ca3ed3 --subnet-id subnet-0ba219ffbd8c264d2 --associate-public-ip-address

Describe-Instance to check PublicDNS

    aws ec2 describe-instances --filter "Name=instance-id,Values=i-078b4a08095f31d35"

Stop Instance

    aws ec2 stop-instances --instance-ids i-078b4a08095f31d35

Start Instance

    aws ec2 start-instances --instance-ids i-078b4a08095f31d35

Add ElasticSearch Pipeline

    curl -XPUT -H 'Content-Type: application/json' 'ec2-35-181-53-159.eu-west-3.compute.amazonaws.com:9200/_ingest/pipeline/nyc_collision' -d @nyc_collision_pipeline.json

Add Elastic Search Template

    curl -XPUT -H 'Content-Type: application/json' 'ec2-35-181-53-159.eu-west-3.compute.amazonaws.com:9200/_template/nyc_collision' -d @nyc_collision_template.json

Send Data using Filebeat

    filebeat -e -c nyc_collision_aws_filebeat.yml 

Check count in ElasticSearch

    curl http://ec2-35-181-53-159.eu-west-3.compute.amazonaws.com:9200/nyc_visionzero/_count

Rows:

    TOTAL: 1.150.000

Index Pattern Kibana

    nyc_visionzero

Add Visualize and Dashboard

    Management tab >> Saved Objects tab >> Import, and select nyc_collision_kibana.json

Terminate instance

    aws ec2 terminate-instances --instance-ids i-078b4a08095f31d35
