### 生成火焰图
~~~
perf record -F 99 -p <pid> -a -g -- sleep 60
perf script -i perf.data &> perf.unfold

使用FlameGraph
./stackcollapse-perf.pl perf.unfold &> perf.folded
./flamegraph.pl perf.folded > perf.svg
~~~
