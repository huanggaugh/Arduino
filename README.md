# Arduino
sensor model for SAFLO(Hardware part)
/* first Prototype Model for SAFLO, finishing connecting the three simple sensor on Arduino. We can inducing the pressure which was been pushed on our product. The part of measuring was done, we still haven't finished to connect to the Blooth model so that we can sent our data to the Firebase.*/


#define fsr_pin1 A0
#define fsr_pin2 A1
#define fsr_pin3 A2
//const byte Back1 = 11;
//const byte Back2 = 12;
//const byte Back3 = 13;

void setup()
{
  //Serial.begin(115200);
  Serial.begin(9600);
  //pinMode(Back1, INPUT_PULLUP);
  //pinMode(Back2, INPUT_PULLUP);
  //pinMode(Back3, INPUT_PULLUP);
  //pinMode(led_pin, OUTPUT);
}

void loop()
{
  int fsr_value1 = analogRead(fsr_pin1); // 讀取FSR
  int fsr_value2 = analogRead(fsr_pin2); // 讀取FSR
  int fsr_value3 = analogRead(fsr_pin3); // 讀取FSR
  //int led_value = map(fsr_value, 0, 1023, 0, 255); // 從0~1023映射到0~255
  //analogWrite(led_pin, led_value); // 改變LED亮度
  //int num1 = analogRead(A0);
  //int num2 = analogRead(A1);
  //int num3 = analogRead(A2);
  
  if(fsr_value1 != 0){

    Serial.print(1);
    Serial.print(" , ");
    Serial.println(fsr_value1);
    
    }
  
    if(fsr_value2 != 0){

    Serial.print(2);
    Serial.print(" , ");
    Serial.println(fsr_value2);
    
    }

    if(fsr_value3 != 0){

    Serial.print(3);
    Serial.print(" , ");
    Serial.println(fsr_value3);
    
    }



  delay(100);
}
