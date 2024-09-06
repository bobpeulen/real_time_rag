# Producer Python file to stream row by row data to OCI Streaming

1. Create compute instance. Oracle Linux 7.
2. Run the below to install Git, clone the repo, and install several packages
  ```
  sudo dnf install git-all -y
  git clone https://github.com/bobpeulen/apache_kafka.git
  sudo pip3 install kafka-python3 pandas numpy datetime
  ```

3. Run the producer. 

```
python apache_kafka/oci_streaming/producer.py  \
-tenancy_name 'oraemeadatamgmt' \
-region 'eu-frankfurt-1' \
-user_name 'OracleIdentityCloudService/bob.peulen@oracle.com' \
-stream_name 'OpenSourceData_stream_1' \
-stream_pool_ocid 'ocid1.streampool.oc1.eu-frankfurt-1.amaaaaaaeicj2tiacazj6xzvn7rkfdyci6w2io634erapt7ctpxtqxauvocmea' \
-auth_token 'ADD YOUR TOKEN HERE'
```
