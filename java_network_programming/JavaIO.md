通信的基础是IO模型

本质上就是数据源到应用的数据交换，从数据源到应用是输入流，从应用到数据源叫输出流

IO流

​    字符流

​		Reader

​		Writer

​	字节流

​		InputStream

​		OutputStream

网络编程中特殊的数据源——socket

socket是网络通信的端点，与本机的端口一一对应，是一个程序层面的逻辑概念

通过socket发送数据

<img src="image/SendDataBySocket.jpeg" alt="SendDataBySocket" style="zoom:50%;" />

1. 创建socket
2. 告诉网卡驱动，将ip和port绑定到socket
3. 发送数据到soket
4. 通过socket将数据发送给驱动程序

通过socket接收数据

<img src="image/ReceiveDataFromSocket.PNG" alt="ReceiveDataFromSocket" style="zoom:50%;" />

1. 创建socket
2. 告诉网卡驱动，将ip和port绑定到socket
3. 网卡接收数据并发送到指定的socket
4. 应用进程从socket接收数据



