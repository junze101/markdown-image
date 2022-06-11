## 搭建open stack云平台



[OpenStack](https://so.csdn.net/so/search?q=OpenStack&spm=1001.2101.3001.7020)云平台搭建需要两个节点，一个是controller（控制节点），另一个是compute（计算节点）。

OpenStack云平台搭建需要两个节点，一个是controller（控制节点），另一个是compute（计算节点）。

控制节点（controller）规划如下：

        一块200G的硬盘。两块网卡，第一块网卡IP地址使用192.168.100.10，第二块网卡IP地址使用192.168.200.10。

计算节点（compute）规划如下：

        一块200G的硬盘和一块100G的硬盘。两块网卡，第一块网卡IP地址使用192.168.100.20，第二块网卡IP地址使用192.168.200.20。
