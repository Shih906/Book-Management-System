## 簡介
本專案為擔任GSS叡揚資訊實習生期間的新人訓練專案，以.NET FrameFork作為後端框架，搭配前端套件Kendo UI，MSSQL作為DataBase，實踐圖書管理系統CRUD

---

## 開發環境
jquery
.NET FrameWork
KendoUI
MSSQL

---

## 說明
根據 ```RouteConfig.cs``` 設定
執行 ```IIS Server``` 後，訪問 ```localhost:55380/BookData/Index```
```C#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.Mvc;
using System.Web.Routing;

namespace NET_MVC_WorkShop2
{
    public class RouteConfig
    {
        public static void RegisterRoutes(RouteCollection routes)
        {
            routes.IgnoreRoute("{resource}.axd/{*pathInfo}");

            routes.MapRoute(
                name: "Default",
                url: "{controller}/{action}/{id}",
                defaults: new { controller = "Home", action = "Index", id = UrlParameter.Optional }
            );
        }
    }
}
```

WebConfig 定義資料庫路徑
```xml
  <connectionStrings>
    <add name="DBConn" connectionString="Data Source=DESKTOP-40A05S2;Initial Catalog=GSSWEB;User ID=sa;Password=123456;" />
  </connectionStrings>
```

---
## Demo
### 查詢書籍
![image](https://github.com/Shih906/Book-Management-System/blob/master/gif/%E6%9F%A5%E8%A9%A2%E6%9B%B8%E7%B1%8D.gif)
### 新增書籍
![image](https://github.com/Shih906/Book-Management-System/blob/master/gif/%E6%96%B0%E5%A2%9E%E6%9B%B8%E7%B1%8D.gif)
### 編輯書籍
![image](https://github.com/Shih906/Book-Management-System/blob/master/gif/%E7%B7%A8%E8%BC%AF%E6%9B%B8%E7%B1%8D.gif)
### 刪除書籍
![image](https://github.com/Shih906/Book-Management-System/blob/master/gif/%E5%88%AA%E9%99%A4%E6%9B%B8%E7%B1%8D.gif)
---

## 開發工具
Microsoft Visual Studio 

![image](https://user-images.githubusercontent.com/88469902/148934026-74a24e50-dcdb-45bc-b3dd-e87fa9223d0d.png)

下載連結 : https://visualstudio.microsoft.com/zh-hant/downloads/
