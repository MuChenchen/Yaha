# Yaha
#define Pin_X A1
#define Pin_Y A0

void setup() {
  Serial.begin(9600);    //串口初始化
  pinMode(Pin_X,INPUT);
  pinMode(Pin_Y,INPUT);
}

void loop() {
  int sensorValueX = analogRead(Pin_X);      //X轴输入
  int sensorValueY = analogRead(Pin_Y);      //Y轴输入
  Serial.print("ValueX:");
  Serial.print(sensorValueX);
  Serial.print(",");
  Serial.print("ValueY:");
  Serial.println(sensorValueY);
  delay(100);
}
