
cocamq

基于netty 的简单mq实现

     网络通讯层netty
     持久层NIO 顺序读写
     broker的负载均衡基于zookeeper

目前完成写入测试

     启动本地zookeeper
     StartServer.java
     MessageProducerTest.java

硬件 mac os 5400 SATA硬盘 I5 2.4Ghz 8GB内存

写入速度

     消息1k   10w循环写   tps 5w/s
     broker 和 producer都是本地运行。
读取速度

    待完成
    利用netty zerocopy

p.s.

   关于写入比较了利用nio Filechannel顺序写 和 MappedByteBuffer 性能表现差不多
   详见MsgFileStorageTest.java和UseMappedFile.java
