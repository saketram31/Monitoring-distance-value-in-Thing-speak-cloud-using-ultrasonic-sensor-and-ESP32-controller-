# Uploading ultrasonic sensor data in Thing Speak cloud
### NAME: R SAKETRAM
### REG.NO : 212223230181

# AIM:
To monitor the distance of the obstacle in the Thing speak cloud using ultrasonic sensor and ESP32 controller.
# Apparatus required:
ESP32 Controller,<br>
Ultrasonic Sensor,<br>
Power supply,<br>
Connecting wires,<br>
Bread board<br>
# PROCEDURE:
## Arduino IDE
Step1:Open the Arduino IDE<br>
Step2: Go to sketch- include library – manage libraries file and install esp32 and thing speak library file<br>
Step3:Go to file and select new file option<br>
Step4:Type the program and update the thing speak channel ID, API key, wifi password and ID<br>
Step5:Go to file and select save option to save the program<br>
Step6:Go to sketch and select verify or compile options<br>
Step7:If no error Hex file will be generated in the temporary folder<br>
Step8: Connect all the components as per the circuit diagram<br>
Step9: Connect the programming cable with esp32 and PC.<br>
Step10: Check the jumper position and connect 4 & 5 of P4.<br>
Step11. Upload the program in the esp32.<br>
Step12 Press the boot button in ESP32 and then press and release the reset button after release the boot button<br>
Step13 Check the output in the cloud<br>
## Thingspeak
Step1 Create a ThingSpeak Account<br>
Step2 Log in to your ThingSpeak account<br>
Step3 Create a new channel by navigating to "Channels" and clicking on "New Channel."<br>
Step4 Configure your channel settings, such as Field labels and Channel name<br>
Step5 Copy the Channel ID and API key in the thingspeak and update in the program<br>
Step6 Execute your program to send the sensor value to ThingSpeak<br>
Step7 Check your ThingSpeak channel to verify that the sensor value has been updated<br>
# THEORY:
## Ultrasonic sensor:
The HC-SR04 is a type of ultrasonic sensor which uses sonar to find out the distance of the object from the sensor. It provides an outstanding range of non-contact detection with high accuracy & stable readings. It includes two modules like ultrasonic transmitter & receiver. This sensor is used in a variety of applications like measurement of direction and speed, burglar alarms, medical, sonar, humidifiers, wireless charging, non-destructive testing, and ultrasonography.
### HC-SR04 Ultrasonic Sensor Pin Configuration
This sensor includes four pins and the pin configuration of this sensor is discussed below.

![image](https://github.com/user-attachments/assets/19050fb2-5138-4a32-85d8-f781f705a0df)


•	Pin1 (Vcc): This pin provides a +5V power supply to the sensor.<br>
•	Pin2 (Trigger): This is an input pin, used to initialize measurement by transmitting ultrasonic waves by keeping this pin high for 10us.<br>
•	Pin3 (Echo): This is an output pin, which goes high for a specific time period and it will be equivalent to the duration of the time for the wave to return back to the sensor.<br>
•	Pin4 (Ground): This is a GND pin used to connect to the GND of the system.<br>
### Features
The features of the HC-SR04 sensor include the following
•	The power supply used for this sensor is +5V DC<br>
•	Dimension is 45mm x 20mm x 15mm<br>
•	Quiescent current used for this sensor is <2mA<br>
•	The input pulse width of trigger is10uS<br>
•	Operating current is 15mA<br>
•	Measuring angle is 30 degrees<br>
•	The distance range is 2cm to 800 cm<br>
•	Resolution is 0.3 cm<br>
•	Effectual Angle is <15°<br>
•	Operating frequency range is 40Hz<br>
•	Accuracy is 3mm<br>
### HC-SR04 Ultrasonic Sensor Working
The HC-SR04 Ultrasonic sensor comes with four pins namely Vcc pin, Trigger pin, Echo pin, & Ground pin. This sensor is used to measure the accurate distance between the target and the sensor. This sensor mostly works on the sound waves.
When the power supply is given to this module, it generates the sound waves to travel throughout the air to hit the necessary object. These waves strike and come back from the object, then collects by the receiver module.
Here both the distance as well as time has taken is directly proportional because the time taken for more distance is high. If the trigger pin is kept high for 10 µs, then the ultrasonic waves will be generated which will travel at the sound speed. So it creates eight cycles of sonic burst that will be gathered within the Echo pin. This ultrasonic sensor is interfaced with Arduino to gauge the necessary distance between sensor & object. The distance can be calculated using the following formula.
S = (V x t)/2 <br>
Where the ‘S’ is the required distance<br>
‘V’ is the sound’s speed <br>
‘t’ is the time taken for sound waves to return back after striking the object.<br>
The actual distance can be calculated by dividing its value with 2 as the time will be twice once the waves travel and get back from the sensor.
## What is IoT?
Internet of Things (IoT) describes an emerging trend where a large number of embedded devices (things) are connected to the Internet. These connected devices communicate with people and other things and often provide sensor data to cloud storage and cloud computing resources where the data is processed and analyzed to gain important insights. Cheap cloud computing power and increased device connectivity is enabling this trend.IoT solutions are built for many vertical applications such as environmental monitoring and control, health monitoring, vehicle fleet monitoring, industrial monitoring and control, and home automation.

![image](https://github.com/user-attachments/assets/493f5a4f-9e29-44b4-8ae7-176879daf5e4)

 
Sending Data to Cloud with ESP32 and ThingSpeak
ThingSpeak is an Internet of Things (IoT) analytics platform that allows users to collect, analyze, and visualize data from sensors or devices connected to the Internet. It is a cloud-based platform that provides APIs for storing and retrieving data, as well as tools for data analysis and visualization.The Internet of Things ( or IoT) is a network of interconnected computing devices such as digital machines, automobiles with built-in sensors, or humans with unique identifiers and the ability to communicate data over a network without human intervention.Hello readers, I hope you all are doing great. In this tutorial, we will learn how to send sensor readings from ESP32 to the ThingSpeak cloud. Here we will use the ESP32’s internal sensor like hall-effect sensor and temperature sensor to observe the data and then will share that data cloud.
## What is ThingSpeak?

![image](https://github.com/user-attachments/assets/5a35cd2f-6083-47dd-9b4b-7d18a56a8a3e)

It is an open data platform for IoT (Internet of Things). ThingSpeak is a web service operated by MathWorks where we can send sensor readings/data to the cloud. We can also visualize and act on the data (calculate the data) posted by the devices to ThingSpeak. The data can be stored in either private or public channels.ThingSpeak is frequently used for internet of things prototyping and proof of concept systems that require analytics.
Features Of ThingSpeak
ThingSpeak service enables users to share analyzed data through public channels:
ThingSpeak allows professionals to prepare and analyze data for their businesses:
ThingSpeak updates various ThingSpeak channels using MQTT and REST APIs:
Easily configure devices to send data to ThingSpeak using popular IoT protocols.
Visualize your sensor data in real-time.
Aggregate data on-demand from third-party sources.
Use the power of MATLAB to make sense of your IoT data.
Run your IoT analytics automatically based on schedules or events.
Prototype and build IoT systems without setting up servers or developing web software.

![image](https://github.com/user-attachments/assets/c7746b27-dca6-4b9f-9e71-b24f3e57b6c8)

 
# PROGRAM:
```
#include <SoftwareSerial.h>
#include <Adafruit_Sensor.h>

#define triggerpin 8                 // trigger pin connected to the ultrosonic sensor 
#define echopin 9                   // techo pin connected to the ultrosonic sensor 

int duration, inches, cm;
String inputString = "";         // a String to hold incoming data
bool stringComplete = false;     // whether the string is complete
long old_time=millis();
long new_time;
long uplink_interval=30000;      //ms
bool time_to_at_recvb=false;
bool get_LA66_data_status=false;
bool network_joined_status=false;
char rxbuff[128];
uint8_t rxbuff_index=0;

SoftwareSerial ss(10, 11);       // Create a SoftwareSerial port on Arduino pins 10 (RX) and 11 (TX)

void setup() {
  pinMode(triggerpin,OUTPUT);
  pinMode(echopin,INPUT);
  Serial.begin(9600);
  ss.begin(9600);
  ss.listen();

  inputString.reserve(200);
  sensor_t sensor;
  ss.println("ATZ");//reset LA66
}

void loop() {
new_time = millis();
if((new_time-old_time>=uplink_interval)&&(network_joined_status==1)){
    old_time = new_time;
    get_LA66_data_status=false;
    HC04();      
    char sensor_data_buff[128]="\0";            
    snprintf(sensor_data_buff,128,"AT+SENDB=%d,%d,%d,%02X%02X",0,2,2,(short)(inches),(short)(cm));
    ss.println(sensor_data_buff);
  }
  if(time_to_at_recvb==true){
    time_to_at_recvb=false;
    get_LA66_data_status=true;
    delay(1000);    
    ss.println("AT+CFG");    
  }
    while ( ss.available()) {
    char inChar = (char) ss.read();
     inputString += inChar;
    rxbuff[rxbuff_index++]=inChar;
    if(rxbuff_index>128)
    break;
    
      if (inChar == '\n' || inChar == '\r') {
      stringComplete = true;
      rxbuff[rxbuff_index]='\0';
       if(strncmp(rxbuff,"JOINED",6)==0){
        network_joined_status=1;
      }
      if(strncmp(rxbuff,"Dragino LA66 Device",19)==0){
        network_joined_status=0;
      }
      if(strncmp(rxbuff,"Run AT+RECVB=? to see detail",28)==0){
        time_to_at_recvb=true;
        stringComplete=false;
        inputString = "\0";
      }
      if(strncmp(rxbuff,"AT+RECVB=",9)==0){       
        stringComplete=false;
        inputString = "\0";
        Serial.print("\r\nGet downlink data(FPort & Payload) ");
        Serial.println(&rxbuff[9]);
      }
       rxbuff_index=0;
      if(get_LA66_data_status==true){
        stringComplete=false;
        inputString = "\0";
      }
    }
  }

   while ( Serial.available()) {
    char inChar = (char) Serial.read();
    inputString += inChar;
    if (inChar == '\n' || inChar == '\r') {
      ss.print(inputString);
      inputString = "\0";
    }
  }
 
  if (stringComplete) {
    Serial.print(inputString);
    
    // clear the string:
    inputString = "\0";
    stringComplete = false;
  }
}

void HC04()
{
   digitalWrite(triggerpin, LOW);
   delayMicroseconds(2);
   digitalWrite(triggerpin, HIGH);
   delayMicroseconds(10);
   digitalWrite(triggerpin, LOW);
   duration = pulseIn(echopin, HIGH);
   inches = microsecondsToInches(duration);
   cm = microsecondsToCentimeters(duration);
   Serial.print(inches);
   Serial.print("in, ");
   Serial.print(cm);
   Serial.print("cm");
   Serial.println();
}
long microsecondsToInches(long microseconds) 
{
   return microseconds / 74 / 2;
}
long microsecondsToCentimeters(long microseconds) 
{
   return microseconds / 29 / 2;
}

/*function Decoder(bytes, port) {
  // Extract distance from the first two bytes
  var distance = (bytes[0] << 8) + bytes[1];

  // Convert to centimeters (assuming millimeters are being sent)
  var distance_in_cm = distance / 100;

  return {
    "distance": distance_in_cm
  };
}*/
```


# CIRCUIT DIAGRAM:
![WhatsApp Image 2025-11-12 at 10 12 28_395f92be](https://github.com/user-attachments/assets/4babe20a-ea09-4874-9110-c55e01de8e31)

# OUTPUT:
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/f9064960-535b-4536-8344-7c4e7e6370a7" />


# RESULT:
Thus the distance values are updated in the Thing speak cloud using ESP32 controller.

