- 바코드 스캐너 TTL 시리얼 통신전환
'''
#include <SoftwareSerial.h>

SoftwareSerial my(2,3); // RX, TX
void setup() {
  // put your setup code here, to run once:
    Serial.begin(9600);
    my.begin(9600); 
}

void loop() {
  // put your main code here, to run repeatedly:
  if(my.available()){
   '''
''' 
- 이 두 줄은 가능하다 하는것
   // Serial.print((char)my.read());   
   //while(??? == 'n')
'''
'''
- 이코드로 진행
   String barcode =my.readStringUntil('\n');
   Serial.println(barcode);
  } 
 }
 '''