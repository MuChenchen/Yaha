#yaho
//1,屏幕显示部分=============================
#include "U8glib.h"
//2,传感器部分================================
#include <Wire.h>
#include "I2Cdev.h"
//温湿度
#include <AM2321.h>
AM2321 am2321;

#include <SoftwareSerial.h>

const int ledPin =  13;

#include "weather.h"
#include "oled.h"

void setup(void) {
  Serial.begin(115200);
  pinMode(ledPin, OUTPUT);
}

void loop(void) {
  updateSensorData();
  volcd();
}
