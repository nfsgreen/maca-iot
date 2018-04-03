# maca-iot
maca-iot简单的把物联网划分为3部分： 

1.center(命令转发中心) 

2.control-point(控制端:web,app,wechat...) 

3.device-point(设备端:GSM/GPRS/NB-IOT/WIFI/ZIGBEE) 

可以适用于物联网绝大多数场景，其中命令转发中心采用netty框架，支持运行多个实例且允许和nginx实现负载均衡，支持UDP/TCP/HTTP/MQTT等协议,
而存储体系采用高可用的mongoDB数据库作为设备信息采集主存储+mysql设备基础信息辅助存储,
web以及app的消息推送采用rabbitMQ+websocket,
contol-point将会扩展为多个分支，包括用于工业的控制平台，用以展示设备的报警信息和地理位置等和用于民用级别的控制系统。 
目前暂时实现的功能是支持UDP协议传输，已接入SIM800C设备，实现了远程开关控制，温湿度采集以及加速度数据采集器功能并展示推送到相应的web页面上。
