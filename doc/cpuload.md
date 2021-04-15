# cpuload

CPU冲高检测工具cpuload，使用该工具能够将CPU使用率高的进程打印出来。
实现原理, 通过bcc工具精确trace调度轨迹, 统计分析CPU占用率高的进程。

```shell
python /usr/share/bcc/tools/cpuload
-t 计算CPU使用率的周期。单位为毫秒，取值为0~60000，取0则每次发生调度都会打印出线程的信息，默认值为1000。
-n 打印CPU使用率top。默认值为3。
-p 设置CPU使用率的水线，超过时打印。0~100，默认值为90。
-m 设置记录调度轨迹的循环缓冲区大小。1000~1000000，默认值为10000。
```
