Inverter_STM_RS
===============

Inverter soure code on STM32f103, refer to Renesas MCU SH7137

这是一个简单的变频器项目，项目采用STM32作为主控芯片。

2014/10/24 9:00am
完成了按键，12864液晶，SPWM波产生的驱动程序。
BUG:
1.定时器2的参数设置会对液晶显示产生干扰；
2014/10/27 8:35am
修复了之前定时器干扰液晶的bug,发现是定时器中断内程序运行时间过长影响了液晶的时序，
解决办法是优化了中断内的计算，使之占用时间更短，效率更高，减小了对液晶时序的干扰，
几乎看不到影响。

2014/11/12
参考瑞萨的思路重新改写了程序，下午测试相电压显示正常。

2014/11/21
线电压完全稳定正常，接上电机转动，但是力度不足且有振动，在增降频率的时候偶尔出现停转。
2014/12/1 10:10
本版在整体电路板出来之后，仅对端口做了更改，为动程序部分。

2014/12/7  Upload  the V2.0 code to github for the first time,this project can be opened by Keil. It work with the V2.0 Inverter PCB, but it does not work very well, on some frequency it will shake, I am studying  the new algorithm.
