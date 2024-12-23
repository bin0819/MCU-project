---
layout: post
title: Innovative Project Proposal
author: [wenbin tsai]
category: [Lecture]
tags: [jekyll, ai]
---

This homework is to propose an innovative project and describe the key features, list all Design Considerations and the required technologies, then draw the System Block Diagram.

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
## 家用機器狗

### 應用功能說明
1.  居家監控：外出時可隨時查看與自動監測家裡狀況
2.	環境監控：溫度、濕度、亮度、一氧化碳、瓦斯濃度偵測與火警偵測
3.	丟棄垃圾：丟棄小型垃圾至垃圾桶
4.	遞送物品：拿取食物或小型物品與開門
5.	藍芽連線：可與其他智慧家具連線，例如：燈泡、窗簾、音響
6.	戶外陪伴：外出慢跑或散步
7.	移動鬧鐘：早晨一定叫你起床，絕對不讓你賴床，或提醒該工作，並讓你完全擺脫拖延症


### 設計考量與相關技術
**系統設計考量：**<br>
1. 操作方式:六軸機器手臂 
2. 移動方式:四足移動
3. 供電方式:電池＋自動充電
4. 聯網方式:WiFi或BT to 手機

**所需相關技術：**
1. 六軸機器手臂 ＆ 軟式夾子
2. 物品辨識分類：Jetson-Nano + IMX219
3. 電子鼻：氣味感測與辨識 MQ2
4. 行走姿態偵測與控制平衡: ESP32 + MPU6050 + PID controller
5. 溫度濕度感測 & 氣體偵測: HTU21D + MQ2 + MQ7 + MQ135
6. 服務器: 具AI加速(GPU)
7. 影像傳輸: ESP32-CAM
8. 模組影像物件偵測: CSL-YOLO 
9. 任務規劃控制: Mission Planner with Floorplan

### 系統方塊圖
![](https://github.com/bin0819/MCU-project/blob/main/images/FDOG.jpg?raw=true)

### 參考圖片1
![](https://github.com/bin0819/MCU-project/blob/main/images/Boston-Dynamics_Spot.jpg?raw=true)

### 參考圖片2
![](https://github.com/bin0819/MCU-project/blob/main/images/C290fab68ddc8365ff3e4139142ae1e2.jpg?raw=true)

### 參考影片1
<iframe width="1239" height="697" src="https://www.youtube.com/embed/UAG_FBZJVJ8" title="Unbelievable  Robot Dance by Boston dynamics" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### 參考影片2
<iframe width="853" height="480" src="https://www.youtube.com/embed/sbT0A7TsUJo" title="Robot Dog meets Real Dog  // Scrappy&#39;s Adventures" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### 參考影片3
<iframe width="853" height="480" src="https://www.youtube.com/embed/ZXKhgC6LsjQ" title="Boston Dynamics @IMTS 2022" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

---
## Market Analysis (市場分析)
![](https://blog.hubspot.com/hs-fs/hubfs/tam-sam-som.png?width=1200&name=tam-sam-som.png)

### TAM of Future Home Products
The Target Market size (TAM) of Future Home Products is the number of household.<br>

### Taiwan Households = 8.93M (台灣 9百萬戶）
* [Total number of households in Taiwan from 2010 to 2020(in 1,000s)](https://www.statista.com/statistics/330804/taiwan-national-total-number-of-households/#:~:text=By%20the%20end%20of%202020,households%20in%20the%20previous%20year.)

### Japan Households = 57.2M (日本 5千7百萬戶)
* [Number of Households in Japan](https://www.helgilibrary.com/indicators/number-of-households/japan/) 

### American Households = 129.93M (美國 1.3億戶)
* [Number of households in the U.S. from 1960 to 2021(in millions)](https://www.statista.com/statistics/183635/number-of-households-in-the-us/)<br>
* [The average American household consisted of 2.51 people in 2021.](https://www.statista.com/statistics/183648/average-size-of-households-in-the-us/)<br>

<br> 
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*


