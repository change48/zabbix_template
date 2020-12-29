# zabbix_template
Hardware monitoring includes the following four LLd：

temp.discovery  
storage.discovery
Power Discovery
Fan Tray Discovery 
This template comes with the basic interface LLD, no need to add other templates about the interfaces

About temp.discovery, you can use the {#RBNENTITYTEMPDESCR} macro to filter the slots you don’t need.
About  interface LLD, recommended use {#IFDESCR} macro to filter  interfaces you don’t need. I used "port.*" to filter and only keep physical interfaces.
It is recommended to create graphics after the template works normally to integrate all hardware monitoring items, because  hardward LLD is separated so  there is no way to integrate graphics in the template.
It works fine on se800 and se1200 routers SmartEdge OS version 6.2.1.7p1 and 6.2.1.11, because this device is very old and I don’t have more devices so I can’t do more tests, if it doesn’t work on your device  please feel free to modify.

There are two items "Memory (used)" & "CPU Usage AVG (1 minute)" copied from Alexei Nikonov's template Ericsson (RedBack) SE100  Thanks.

If you need help, you can send an email to whye1700#gmail.com(replace # with @)

 ###############################################

爱立信 se800、se1200 snmpv2模板:LLD主要有硬件、接口两个项，其中硬件有

板卡温度LLD
存储LLD
电源LLD
风扇LLD
其中，板卡温度LLD建议使用{#RBNENTITYTEMPDESCR}宏来过滤不需要监控的板卡、接口LLD建议使用{#IFDESCR}宏来过滤仅保留物理接口，另外建议在确认模板正常后在主机建立硬件监控的图形整合多个监控项，因为硬件LLD是分散的所以在一个模板里建立有难度。

仅在se800和se1200的6.2.1.7p1、6.2.1.11两个版本上做了测试，不一定完全适用于所有redback设备，有异常的地方请随意修改。

有两个监控项  "Memory (used)" & "CPU Usage AVG (1 minute)" 拷贝自Alexei Nikonov's template Ericsson (RedBack) SE100。

有关于模板的疑问请邮件到whye1700#gmail.com(replace # with @)
