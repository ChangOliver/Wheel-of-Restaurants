# Web Programming - Final Project Report
## 專題資訊 (Group 28)
+ **題目名稱：** WTF - Where's The Food? (Wheel of Restaurants)
+ **簡介：**
    + 民以食為天。對於學生來說，今天吃什麼是每天必須思考的燒腦問題。因此，我們發想了一個可以客製化的餐廳轉盤，讓大家不僅不需花費腦力思考這個問題，還能從轉盤中得到些許驚喜感。除此之外，使用者也能自行編輯最愛以及不喜歡的餐廳清單，客製化轉盤上的選項。現在就讓轉盤來告訴你「Where's the food」吧！
+ **[Deployed 連結](https://lin9999.github.io/Wheel-of-Restaurants/)**
+ **[Demo 影片連結](https://www.youtube.com/watch?v=sO03RFtJH7E)**

## 使用方式＆功能介紹
### local啟動服務
+ Server： ```yarn server```
+ Client： ```yarn start```
### Login / Register
+ 使用者視角:
    + 在對應的欄位輸入使用者名稱及密碼，若帳號不存在或密碼錯誤皆無法登入。
![](https://i.imgur.com/xqxWmFk.png)
+ Server 
+ Client
### The Wheel
+ 使用者視角:
    + 轉盤下方有欄位可供使用者選擇轉盤上的餐廳數量
    + 新使用者
![](https://i.imgur.com/EG2sisK.png)
    + 有建立最愛清單之使用者 (預設由清單中選三個)
![](https://i.imgur.com/SuT1km4.png)
+ Server
+ Client
### All / Favorite / Blacklist Tabs
+ 使用者視角:
![](https://i.imgur.com/5tFW24l.png)
+ Server
+ Client
### Google Map
+ 使用者視角:
+ ![](https://i.imgur.com/QAC3mEn.png)
+ Server
+ Client

## Future Works
+ 忘記密碼(Forget Password)
+ 擴大範圍、包含更多餐廳
+ 使用者框出一個區域後，系統自行帶入範圍內所有餐廳至轉盤上
+ Admin專用頁面，用以管理餐廳及使用者資料
## 分工＆製作心得：
+ 張原豪 (B06902119)
    + 貢獻：CSS介面設計、Login/Register、清單功能實作、Demo Video 剪輯
    + 心得：
+ 林恩廷 (B06902023)
    + 貢獻：Backend、資料庫處理、前後端溝通、Deployment
    + 心得：
+ 林晉辰 (B05505019)
    + 貢獻：轉盤功能實作、使用者資訊加密、清單功能實作
    + 心得：
## 參考資料＆使用之套件、框架、程式碼
+ Frontend：
    + React.js
    + react hooks
    + axios
    + [Ant Design](https://ant.design/components/overview/)
    + [spinning-wheel-game-react](https://github.com/hadriengerard/spinning-wheel-game-react/tree/master/)
+ Backend：
    + Node.js
    + express
    + bcrypt
+ Database： 
    + [MongoDB](https://www.mongodb.com/1)
    + mongoose
