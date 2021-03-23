# ConsoleApp20210324

VS2017 C# MYSQL資料庫開發(.Net Core主控台應用程式)+linux群輝NAS部屬docker

參考資料:
https://docs.microsoft.com/zh-tw/azure/mysql/connect-csharp
http://yhhuang1966.blogspot.com/2017/11/xampp-php.html
http://www.coolsun.idv.tw/modules/xhnewbb/viewtopic.php?topic_id=1510
https://anglerdiy.com/?p=2563
https://ithelp.ithome.com.tw/articles/10218214


程式碼:https://github.com/eric19740521/ConsoleApp20210324

1.xampp,mysql安裝
http://yhhuang1966.blogspot.com/2017/11/xampp-php.html


2.mySQL管理工具(Navicat_Portable_v12.0.17/phpMyAdmin)
https://softblog.tw/navica.html



3.vs2017 安裝/vscode
https://my.visualstudio.com/Downloads?q=visual%20studio%202017&wt.mc_id=o~msft~vscom~older-downloads


4.引用
using MySql.Data;
using MySql.Data.MySqlClient;



6.群輝NAS Docker
倉庫伺服器 找尋 microsoft dotnet

設定 儲存空間
docker/test   /test






           String str="";

            var db = new nameDBClass.DBClass();


            //
            db.dbHost = "192.168.1.21";//資料庫位址
            db.dbUser = "sa";//資料庫使用者帳號
            db.dbPass = "661ho728";//資料庫使用者密碼
            db.dbName = "test";//資料庫名稱

            //建立資料庫test01
            db.CreateDB();
            str=db.GetReturnMsg(); 
            Console.WriteLine(str);

            //建立使用者帳號密碼 權限
            db.CreateUser();
            str = db.GetReturnMsg();
            Console.WriteLine(str);


            //用剛建立的資料庫與使用者連線
            db.dbHost = "192.168.1.21";//資料庫位址
            db.dbUser = "user";//資料庫使用者帳號
            db.dbPass = "password";//資料庫使用者密碼
            db.dbName = "test01";//資料庫名稱

            //
            db.CreateTable();
            str = db.GetReturnMsg();
            Console.WriteLine(str);

            //
            db.CreateSP();
            str = db.GetReturnMsg();
            Console.WriteLine(str);


            //
            db.MemberInsert();
            str = db.GetReturnMsg();
            Console.WriteLine(str);

            //
            db.MemberList();
            str = db.GetReturnMsg();
            Console.WriteLine(str);

            //
            db.MemberList2();
            str = db.GetReturnMsg();
            Console.WriteLine(str);

            //
            db.MemberUpdate();
            str = db.GetReturnMsg();
            Console.WriteLine(str);


            //
            db.MemberDelete();
            str = db.GetReturnMsg();
            Console.WriteLine(str);

            //
            db.MemberDelAll();
            str = db.GetReturnMsg();
            Console.WriteLine(str);









