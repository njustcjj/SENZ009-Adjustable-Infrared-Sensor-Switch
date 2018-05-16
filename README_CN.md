# SENZ009 红外光电开关、避障传感器

###### 翻译

> `英文` 请参考 [`这里`](https://github.com/njustcjj/SENZ009-Adjustable-Infrared-Sensor-Switch/blob/master/README.md)

> `中文` 请参考 [`这里`](https://github.com/njustcjj/SENZ009-Adjustable-Infrared-Sensor-Switch/blob/master/README_CN.md)

![](https://github.com/njustcjj/SENZ009-Adjustable-Infrared-Sensor-Switch/blob/master/pic/SENZ009.jpg "SENZ009")
 

### 产品介绍

> SENZ009是一种集发射与接收于一体的光电开关传感器。数字信号的输出伴随传感器后侧指示灯亮的亮灭，检测距离可以根据要求进行调节。该传感器具有探测距离远、受可见光干扰小、价格便宜、易于装配、使用方便等特点。

> 
> 用途：机器人避障、互动媒体、工业自动化流水线等

### 产品参数

* 信号类型：数字输出
- 工作电压：5V DC
- 电流：<100mA
- 探测距离：3～80cm
- 探头直径：18 mm
- 探头长度：45 mm
- 电缆长度：45 cm
- 响应时间：< 2ms
- 工作环境温度：-25 ~ +55 ℃


### 使用教程

#### 接线定义

|Sensor wire|Ardunio Pin|Function Description|
|-|:-:|-|
|红色线|3.3V~5V|Power|
|蓝色线|GND||
|黑色线|Digital pin|Digital Output|



![](https://github.com/njustcjj/SENZ009-Adjustable-Infrared-Sensor-Switch/blob/master/pic/SENZ009_pin.jpg "引脚定义") 


#### 连线图

![](https://github.com/njustcjj/SENZ009-Adjustable-Infrared-Sensor-Switch/blob/master/pic/SENZ009_connect.png "连线图") 


### 示例代码

	const int InfraredSensorPin = 4;//Connect the signal pin to the digital pin 4
	const int LedDisp = 13;

	void setup()
	{
	  Serial.begin(57600);
	  Serial.println("Start!");  
	  pinMode(InfraredSensorPin,INPUT);
	  pinMode(LedDisp,OUTPUT);
	  digitalWrite(LedDisp,LOW);
	}

	void loop()
	{
	  if(digitalRead(InfraredSensorPin) == LOW)  digitalWrite(LedDisp,HIGH);
	  else  digitalWrite(LedDisp,LOW);
	  Serial.print("Infrared Switch Status:");
	  Serial.println(digitalRead(InfraredSensorPin),BIN);
	  delay(50);
	}


### 购买[*SENZ009 红外光电开关、避障传感器*](https://www.ebay.com/).