## 簡介
本專案為擔任GSS叡揚資訊實習生期間的新人訓練專案，以.NET FrameFork作為後端框架，搭配前端套件Kendo UI，MSSQL作為DataBase，實踐圖書管理系統CRUD

---

## 開發環境
jquery
.NET FrameWork
KendoUI
MSSQL

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
## 開發工具
Microsoft Visual Studio 

![image](https://user-images.githubusercontent.com/88469902/148934026-74a24e50-dcdb-45bc-b3dd-e87fa9223d0d.png)

下載連結 : https://visualstudio.microsoft.com/zh-hant/downloads/
