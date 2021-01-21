# Web Programming - Final Project Report
## 專題資訊 (Group 28)
+ **題目名稱：** WTF - Where's The Food? (Wheel of Restaurants)
+ **簡介：**
    + 民以食為天。對於學生來說，今天吃什麼是每天必須思考的燒腦問題。因此，我們發想了一個可以客製化的餐廳轉盤，讓大家不僅不需花費腦力思考這個問題，還能從轉盤中得到些許驚喜感。除此之外，使用者也能自行編輯最愛以及不喜歡的餐廳清單，客製化轉盤上的選項。現在就讓轉盤來告訴你「Where's the food」吧！
+ **[Deployed 連結](https://lin9999.github.io/Wheel-of-Restaurants/)**
+ **[Demo 影片連結](https://www.youtube.com/watch?v=sO03RFtJH7E)**

## 使用方式＆功能介紹
### Hosting on local machine
+ 安裝 modules
```
yarn   
cd frontend && yarn
cd ../backend && yarn
```
+ 在backend建立.env檔案並提供MongoDB連結
+ 啟動
    + Server： ```yarn server```
    + Client： ```yarn start```
### Login / Register
+ 畫面: ![](https://i.imgur.com/xqxWmFk.png)
+ 功能：
    + 提供登入與註冊的功能。需在對應的欄位輸入使用者名稱及密碼（不可空白），若帳號不存在或密碼錯誤皆無法登入。
+ 實作細節：
    + 登入時使用username與password找到對應使用者的UID，並取出所有相關資料
    + 註冊時即把使用者資訊寫入資料庫，並自動登入
    + 若有任何error，則把錯誤訊息顯示於訊息欄中
### The Wheel
+ 畫面:
    + 新使用者
![](https://i.imgur.com/EG2sisK.png)
    + 有建立最愛清單之使用者 (預設由最愛清單中選三個)
![](https://i.imgur.com/SuT1km4.png)
+ 功能：
    + 轉盤下方有欄位可供使用者選擇轉盤上的餐廳數量
    + 預設由使用者的最愛清單中選出三家餐廳
    + 點擊轉盤即可開始抽獎
+ 實作細節：
    + 轉盤根據Wheel餐廳數量平均分割。
    + 在點擊的瞬間決定抽選的結果，並透過css來實現轉盤旋轉的動畫，並且控制右方的地圖在合理的時間點顯示資訊
    + 從加入Wheel中的選項中隨機選取一個ID，並透過CSS轉到這家餐廳。
    + Choises的數量是透過Filter來減少Wheel上的餐廳。
### All / Favorite / Blacklist Tabs
+ 畫面:
    + 所有餐廳
![](https://i.imgur.com/5tFW24l.png)
    + 最愛清單（黑名單亦同）
![](https://i.imgur.com/QANooy4.png)

+ 功能：
    + 提供所有的餐廳列表，可以透過搜尋的方式找到餐廳資訊，也可以讓當前使用者建立客製化列表，以利之後再次使用時能夠更快的決定想要加入的餐廳
    + 餐廳底下提供簡易資訊如：價格、種類、地點
    + 點擊按鈕可將餐廳新增至轉盤/最愛清單/黑名單，也可從清單中移除餐廳
    + 已新增至最愛清單的餐廳不能新增至黑名單，反之亦然
    + 點擊餐廳名稱可由Google Map得到更多相關資訊
+ 實作細節：
    + 利用filter來選出要顯示的餐廳，且當使用者將餐廳加入黑白名單時，會同時更新資料庫的紀錄，讓使用者隨時登出都不會影響到名單的儲存
    + 利用Ant Design實作不同的獨立的Tab
### Google Map
+ 畫面： ![](https://i.imgur.com/QAC3mEn.png)
+ 功能：
    + 利用Google提供更多餐廳資訊，即時顯示抽到的餐廳的位置、評論等等。
+ 實作細節：
    + 插入GoogleMap iframe，使用事先儲存於database的網址作為src

### Developer's Page
+ 畫面：![](https://i.imgur.com/KNOar8l.png)
+ 功能：
    + 讓管理者能更方便的新增餐廳資訊，管理餐廳清單及使用者清單
+ 實作細節：
    + 將表格中的資料寫入資料庫，或刪除所有資料

## Future Works
+ 忘記密碼(Forget Password)
+ 擴大範圍、包含更多餐廳
+ 使用者框出一個區域後，系統自行帶入範圍內所有餐廳至轉盤上
+ 可透過更多方式搜尋餐廳(價位、樣式、地區等等)
+ Admin專用頁面，用以管理餐廳及使用者資料
## 分工＆製作心得：
+ 張原豪 (B06902119)
    + 貢獻：CSS介面設計、Login/Register、清單功能實作、Demo Video 剪輯
    + 心得：做了project才知道平常看似簡單的網頁功能其實背後卻一點也不簡單。尤其是網頁的設計會直接影響到使用者在使用上的便利性，光是設計介面就花了許多時間在做調整。也了解到當組員們各司其職開發功能時互相溝通的重要性，才能在過程中用最有效率的方式完成一個網頁。
+ 林恩廷 (B06902023)
    + 貢獻：Backend、資料庫處理、前後端溝通、Deployment
    + 心得：以往課程的project大多都是在特殊取向的情形下做的，說實話實用度幾乎接近於零，但這次的作品卻讓我感受到自己真的可以做出點什麼接近大眾使用的東西。透過這次project我也覺得網頁開發真的是五花八門，一個問題上網找就會有各種不同工具之間搭配得到的解法，而在分工上我認為也是最容易的一個語言了，可能也是因為本身幾乎就是物件的集合體的關係，不用特別下功夫就能將自己做的東西與別人銜接，做出最後的成品。
+ 林晉辰 (B05505019)
    + 貢獻：轉盤功能實作、使用者資訊加密、清單功能實作
    + 心得：這次的Project讓我學到比較完整的網頁服務，包含了前端、後端、資料庫。以前我學網頁的時候都只用HTML/CSS/JavaScript寫，而這個project讓我學到如何使用框架來完成一個網路服務，也讓我未來能夠比較有架構的寫一個網頁。而這次Project中遇到最大的困難應該如何在各個Component之間傳送資料，以及state的控制。有時候發現state沒有變化，就是因為有state dependency的問題。
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
