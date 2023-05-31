---
layout: post
title: IoT-Thinkspeak.com
author: [wenbin tsai]
category: [Lecture]
tags: [jekyll, ai]
---


This homework is to propose robot car, list all Design Considerations and the required technologies, then draw the System Block Diagram.

---
## Homework Report Format
**Contents:**<br>
* **應用與功能說明**
  - Specify the future home application, and Describe the key features
  - Describe the key features which may be applied to the home space (kitchen, living room, play room, study room, bed room)
* **設計考量與所需相關技術**
  - List all design considerations and the required technologies
* **系統方塊圖**
  - Draw a System Block Diagram
---

### IoT-Thinkspeak.com

### 目錄
1. 應用功能說明
2. 所需相關物件
3. 系統方塊圖
4. 成品展示
5. 程式碼

### 應用功能說明
將DHT11感測的溫度與濕度藉由WiFi上傳至Thinkspeak.com上，並將其繪製成圖表

### 所需相關物件：
1. ESP32
2. 傳輸線
3. DHT11:感測溫度與濕度




### 系統方塊圖
![](https://github.com/bin0819/MCU-project/blob/main/images/B111111.jpg?raw=true)
### Thinkspeak.com
![](https://github.com/bin0819/MCU-project/blob/main/images/B111.png?raw=true)


### 成品
![](https://github.com/bin0819/MCU-project/blob/main/images/B1111.jpg?raw=true)


### 成品展示
<iframe width="320" height="560" src="https://www.youtube.com/embed/tS6ctpU4K7I" title="2023年5月25日" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

-------------------------
### 程式碼

```

/*
 *  This sketch sends data via HTTP GET requests to thingspeak service every 10 minutes
 *  You have to set your wifi credentials and your thingspeak key.
 */

#include <WiFi.h>

#include "DHT.h"

#define DHTPIN 23     // NodeMCU pin D6 connected to DHT11 pin Data
DHT dht(DHTPIN, DHT11, 15);

const char* ssid     = "A51";
const char* password = "0905050920";




const char* host = "api.thingspeak.com";
const char* thingspeak_key = "SXSG4CLWO7UKE4KB";

void turnOff(int pin) {
  pinMode(pin, OUTPUT);
  digitalWrite(pin, 1);
}

void setup() {
  Serial.begin(115200);

  // disable all output to save power
  turnOff(0);
  turnOff(2);
  turnOff(4);
  turnOff(5);
  turnOff(12);
  turnOff(13);
  turnOff(14);
  turnOff(15);

  dht.begin();
  delay(10);
  

  // We start by connecting to a WiFi network

  Serial.println();
  Serial.println();
  Serial.print("Connecting to ");
  Serial.println(ssid);
  
  WiFi.begin(ssid, password);
  
  while (WiFi.status() != WL_CONNECTED) {
    delay(500);
    Serial.print(".");
  }

  Serial.println("");
  Serial.println("WiFi connected");  
  Serial.println("IP address: ");
  Serial.println(WiFi.localIP());
}

int value = 0;

void loop() {
  delay(5000);
  ++value;

  Serial.print("connecting to ");
  Serial.println(host);
  
  // Use WiFiClient class to create TCP connections
  WiFiClient client;
  const int httpPort = 80;
  if (!client.connect(host, httpPort)) {
    Serial.println("connection failed");
    return;
  }

  String temp = String(dht.readTemperature());
  String humidity = String(dht.readHumidity());
  //String voltage = String(system_get_free_heap_size());
  String url = "/update?key=";
  url += thingspeak_key;
  url += "&field1=";
  url += temp;
  url += "&field2=";
  url += humidity;
  
  Serial.print("Requesting URL: ");
  Serial.println(url);
  
  // This will send the request to the server
  client.print(String("GET ") + url + " HTTP/1.1\r\n" +
               "Host: " + host + "\r\n" + 
               "Connection: close\r\n\r\n");
  delay(10);
  
  // Read all the lines of the reply from server and print them to Serial
  while(client.available()){
    String line = client.readStringUntil('\r');
    Serial.print(line);
  }
  
  Serial.println();
  Serial.println("closing connection. going to sleep...");
  delay(100);
  // go to deepsleep for 1 minutes
  //system_deep_sleep_set_option(0);
  //system_deep_sleep(1 * 60 * 1000000);
  delay(1*1*100);
}
  
  ```
--------------------------
<br> 
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*
