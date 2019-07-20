# potentio
this code used **potentio**

## parts list

* arduino
* LED
* wire
* potentio
* breadboard


## arduino code

```cpp
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  pinMode(2,OUTPUT);
  pinMode(3,OUTPUT);
  pinMode(4,OUTPUT);
  pinMode(5,OUTPUT);
}

void loop() {
  // put your main code here, to run repeatedly:

 
  int value;
  value=analogRead(A0);

  //Serial.println(value);

  if(value<200) {
   digitalWrite(2,LOW);
   digitalWrite(3,LOW);
   digitalWrite(4,LOW);
   digitalWrite(5,LOW);
  }else if(value<400) {
   digitalWrite(2,HIGH);
   digitalWrite(3,LOW);
   digitalWrite(4,LOW);
   digitalWrite(5,LOW);
  }else if(value<600) {
   digitalWrite(2,LOW);
   digitalWrite(3,HIGH);
   digitalWrite(4,LOW);
   digitalWrite(5,LOW);
  }else if(value<800) {
   digitalWrite(2,LOW);
   digitalWrite(3,LOW);
   digitalWrite(4,HIGH);
   digitalWrite(5,LOW);
  }else{
   digitalWrite(2,LOW);
   digitalWrite(3,LOW);
   digitalWrite(4,LOW);
   digitalWrite(5,HIGH);
}
}

```
![arduino LED]
















