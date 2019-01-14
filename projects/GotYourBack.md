---
layout: project
type: project
published: true
image: ../images/Arduino.png
published: true
title: GotYourBack
# All dates must be YYYY-MM-DD format!
date: 2017-11-22
labels:
  - Arduino
  - MIT App Inventor
summary: Designed a wearable security alarm system.
---

In a team of two, we created a wearable security alarm. We used Arduino and MIT App Inventor to implement our design.

Using an IR sensor we were able to calculate the distance of an attacker approximately 4 feet away. If the sensor were to pick up motion the alarm would send a signal to the users phone. An app that was designed by my partner would then imediately call the users emergency contant or set of an alarm on the users phone. 

My role in the project was to implment the IR sensor and Arduino. Once the sensor detected something a signal would be sent to the app.
Here is the code that I used to program the Arduino:
```c
//define pins
int dist_pin = 0;

//save distance reading
int current_dist = 0;
int sensor_dist= 0;

void setup() {
 Serial.begin(9600);

}

void loop() {
 
 //read in the sensor distance
 sensor_dist = analogRead(dist_pin);
 
 //convert into cm
 current_dist=28250/(sensor_dist - 229.5);

 //check to see if there is an accurate reading
 //if there is a weird reading i.e negative/ large reading read again
 while(current_dist < 0 || current_dist> 500){
   sensor_dist = analogRead(dist_pin);
   //convert into cm
   current_dist=28250/(sensor_dist - 229.5);
 }
  
 //for debug, print the values on the monitor
 //Serial.print(current_dist);
 //Serial.println("cm");

   //check to see if the attacker is about 4 feet away
   //if yes then set alarm off
  if(current_dist < 130){
   //set alarm off
   Serial.write("alarm");
  }
  
 //delay by half a second
 delay(500);
}
```
