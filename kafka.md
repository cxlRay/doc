* Kafka broker stop - java.io.IOException: Map failed
~~~
sysctl vm.max_map_count
sysctl -w vm.max_map_count=655300
cat /proc/[kafka-pid]/maps | wc -l
~~~
