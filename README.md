# SENZ009-Adjustable-Infrared-Sensor-Switch

###### Translation

> For `English`, please click [`here.`](https://github.com/njustcjj/SENZ009-Adjustable-Infrared-Sensor-Switch/blob/master/README.md)

> For `Chinese`, please click [`here.`](https://github.com/njustcjj/SENZ009-Adjustable-Infrared-Sensor-Switch/blob/master/README_CN.md)

![](https://github.com/njustcjj/SENZ009-Adjustable-Infrared-Sensor-Switch/blob/master/pic/SENZ009.jpg "SENZ009")


### Introduction

>  The DFRobot Adjustable Infrared Sensor Switch is a set of transmitter and receiver in one of the photoelectric switch sensor. The detection distance can be adjusted according to the demand. The DFRobot Adjustable Infrared Sensor Switch is small, easy to use, inexpensive, easy to assemble. The switching signal output differs in accordance to the obstacles. It remains high when no obstacles and remains low when there are obstacles. There is also a red led on its back to indicate the sensor status.
>
> Usage : robot to avoid obstacles, interactive media, industrial assembly line, and etc.



### Specification

- Power supply: 5V
- Working Current: <100mA
- Adjustable detection range: 3cm - 80cm
- Digital output:
	- "0" - found barrier (~0V)
	- "1" - no barrier (~4V)
- Dimension: 45 x Φ18 mm

### Tutorial

#### Wire Definition

|Sensor wire|Ardunio Pin|Function Description|
|-|:-:|-|
|Red wire|3.3V~5V|Power|
|Blue wire|GND||
|Black wire|Digital pin|Digital Output|

![](https://github.com/njustcjj/SENZ009-Adjustable-Infrared-Sensor-Switch/blob/master/pic/SENZ009_pin.jpg "Pin Definition") 

#### Connecting Diagram

![](https://github.com/njustcjj/SENZ009-Adjustable-Infrared-Sensor-Switch/blob/master/pic/SENZ009_connect.png "Connecting Diagram") 

#### Sample Code


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


### Purchasing [*SENZ009 Adjustable Infrared Sensor Switch*](https://www.ebay.com/).
