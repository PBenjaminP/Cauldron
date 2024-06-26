# Cauldron
HackMD co-documentary
https://g0v.hackmd.io/s/BkGmY2jV0

IOS code
由於iOS的系統限制，請注意，這個應用只能在用戶主動使用時追蹤活動，不能在背景持續運行或追蹤其他應用的使用情況。
近端佈署代碼：
1.	在Xcode中創建一個新的iOS應用項目。
2.	添加一個Core Data模型，命名為"ActivityModel"，並創建一個名為"Activity"的實體，包含"name"(String)、"duration"(Integer)和"date"(Date)屬性。
3.	在Main.storyboard中設置相應的UI元素。
4.	將這段代碼添加到項目中。

Android code
近端佈署代碼:
1.	在Android Studio中創建一個新的Android項目。
2.	創建相應的Java文件並添加這些代碼。
3.	在res/layout/activity_main.xml中設置相應的UI元素。
4.	在AndroidManifest.xml中添加服務聲明和必要的權限:
<manifest ...>
    <uses-permission android:name="android.permission.FOREGROUND_SERVICE" />
    <application ...>
        ...
        <service android:name=".TrackerService" />
    </application>
</manifest>
代碼目前只提供了基本功能,並且可以在後台運行一段時間。然而,Android系統可能在一段時間後終止服務以節省電池。
在實際應用中,還需要添加更多的錯誤處理、UI改進、數據導出功能,以及可能的定期同步機制來確保數據不會丟失。
