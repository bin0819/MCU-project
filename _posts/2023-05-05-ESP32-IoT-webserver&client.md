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
2. 系統設計考量
3. 所需相關物件
4. 系統方塊圖
5. 成品展示
6. 程式碼

### 應用功能說明
以藍芽或Wife連線來控制自走車，使其前進、後退或左右轉


### 設計考量與相關技術
**系統設計考量：**<br>
1. 操作方式:手機點擊控制 
2. 移動方式:兩輪移動
3. 供電方式:電池
4. 聯網方式:WiFi或BT to 手機

**所需相關物件：**
1. 自走小車套件
2. 鋰電池:提供3.7V電壓
3. 行動電池盒:固定兩顆電池
5. 直流馬達:轉動輪子使其移動
6. L7805CV:穩壓IC提供穩定電壓5V
7. DRV8833:直流馬達驅動板控制直流馬達
8. ESP32:提供藍芽或Wife連線並控制DRV883

### 系統方塊圖
![](https://github.com/bin0819/MCU-project/blob/main/images/AA444.JPG?raw=true)

### 成品
![](https://github.com/bin0819/MCU-project/blob/main/images/AA123.jpg?raw=true)

### 前進
<iframe width="435" height="774" src="https://www.youtube.com/embed/vw0Oo5jidaM" title="forwork" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### 後退
<iframe width="435" height="774" src="https://www.youtube.com/embed/sw4PZcQTnek" title="back" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### 左轉
<iframe width="435" height="774" src="https://www.youtube.com/embed/8leGL-gKyak" title="left" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### 右轉
<iframe width="435" height="774" src="https://www.youtube.com/embed/fDQ0pliakaQ" title="right" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

-------------------------
### 程式碼

![](https://github.com/bin0819/MCU-project/blob/main/images/A1.png?raw=true)
![](https://github.com/bin0819/MCU-project/blob/main/images/A2.png?raw=true)
![](https://github.com/bin0819/MCU-project/blob/main/images/A3.png?raw=true)
![](https://github.com/bin0819/MCU-project/blob/main/images/A4.png?raw=true)
![](https://github.com/bin0819/MCU-project/blob/main/images/A5.png?raw=true)
--------------------------
<br> 
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*
---
layout: post
title: ESP32-OTA
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
2. 系統設計考量
3. 所需相關物件
4. 系統方塊圖
5. 成品展示
6. 程式碼

### 應用功能說明
以藍芽或Wife連線來控制自走車，使其前進、後退或左右轉


### 設計考量與相關技術
**系統設計考量：**<br>
1. 操作方式:手機點擊控制 
2. 移動方式:兩輪移動
3. 供電方式:電池
4. 聯網方式:WiFi或BT to 手機

**所需相關物件：**
1. 自走小車套件
2. 鋰電池:提供3.7V電壓
3. 行動電池盒:固定兩顆電池
5. 直流馬達:轉動輪子使其移動
6. L7805CV:穩壓IC提供穩定電壓5V
7. DRV8833:直流馬達驅動板控制直流馬達
8. ESP32:提供藍芽或Wife連線並控制DRV883

### 系統方塊圖
![](https://github.com/bin0819/MCU-project/blob/main/images/AA444.JPG?raw=true)

### 成品
![](https://github.com/bin0819/MCU-project/blob/main/images/AA123.jpg?raw=true)

### 前進
<iframe width="435" height="774" src="https://www.youtube.com/embed/vw0Oo5jidaM" title="forwork" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### 後退
<iframe width="435" height="774" src="https://www.youtube.com/embed/sw4PZcQTnek" title="back" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### 左轉
<iframe width="435" height="774" src="https://www.youtube.com/embed/8leGL-gKyak" title="left" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### 右轉
<iframe width="435" height="774" src="https://www.youtube.com/embed/fDQ0pliakaQ" title="right" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

-------------------------
### 程式碼

![](https://github.com/bin0819/MCU-project/blob/main/images/A1.png?raw=true)
![](https://github.com/bin0819/MCU-project/blob/main/images/A2.png?raw=true)
![](https://github.com/bin0819/MCU-project/blob/main/images/A3.png?raw=true)
![](https://github.com/bin0819/MCU-project/blob/main/images/A4.png?raw=true)
![](https://github.com/bin0819/MCU-project/blob/main/images/A5.png?raw=true)
--------------------------
<br> 
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*
