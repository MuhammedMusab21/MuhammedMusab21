#include <Servo.h>                                     //sevonun kütüphanesine ba?lan?yoruz
//integerlar? tan?ml?yoruz
int suPin=A0;                                         //su sens�r�n� ba?layaca??m?z pin
int esikDegeri=100;                                   //su miktar? için eşik değeri      
int veri;                                             // sens�rden gelen de?er                                                                                
int servo1=10;                                        //sa?daki servoyu ba?layaca??m?z pin
int servo2=7;                                         //ortadaki servoyu bağlayacağımız pin
int servo3=4;                                         //soldaki servoyu bağlayacağımız pin
int hareket1;
int hareket2;
int hareket3;                                         
Servo motor1;
Servo motor2;
Servo motor3;
//ba?lad?�?m?z malzemelerin giri? veya �?k?? pini oldu?unu tan?ml?yoruz
void setup()
{
motor1.attach(servo1);
motor2.attach(servo2);
motor3.attach(servo3);
}
//void loopa kodumuzu yaz?yoruz
void loop()
{
veri = analogRead(suPin);
if (veri > esikDegeri)
{
motor3.write(90);
}
else 
{
motor3.write(0);
}
if (hareket2==1)
{
motor2.write(90);
delay(5000);
motor2.write(0);
}
if (hareket1==1)
{
motor1.write(90);
delay(10000);
motor1.write(0);
}}
