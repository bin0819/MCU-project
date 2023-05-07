---
layout: post
title: ESP32 IoT webserver & client
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

###  RoboCar

### 目錄
1. 應用功能說明
2. 所需相關物件
3. 系統方塊圖
4. 成品展示
5. 程式碼

### 應用功能說明
其中一片ESP32為webserver，另一片為client，並在其上連接溫溼度感測器，並將資料傳送至webserver架構的網站


**所需相關物件：**
1. ESP32*2
2. 傳輸線*2
3. HTU21DF溫濕度感測器


### 系統方塊圖
![](https://github.com/bin0819/MCU-project/blob/main/images/AA8888.jpg?raw=true)

### 成品

**表格：**<br>
![](https://github.com/bin0819/MCU-project/blob/main/images/AA8.jpg?raw=true)

**#client：**
![](https://github.com/bin0819/MCU-project/blob/main/images/AA88.png?raw=true)

**webserver：**
![](https://github.com/bin0819/MCU-project/blob/main/images/AA888.png?raw=true)


-------------------------
### 程式碼
**webserver：**<br>
1111

**client：**
2222

--------------------------
<br> 
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*
---


