ShadowsocksR for Windows
=======================

[![Build Status]][Appveyor]

#### Download

You will need to download and install [7-Zip](http://www.7-zip.org/) in order 
to extract the ShadowsocksR archive.

Download the [latest release] for ShadowsocksR for Windows.

_Optionally_, right-click on the downloaded 7z file and select 
**CRC SHA** > **SHA-256**. Verify that the SHA-256 checksum displayed 
matches the expected checksum which was shown on the releases page.

Right-click on the downloaded 7z file and do **7-Zip** > **Extract Here** 
or extract to a new folder.

_Optionally_, download and install [Gpg4win](https://www.gpg4win.org/). 
From the Windows start menu, launch program **Kleopatra**. 
Do **File** > **New Certificate** to create a personal OpenPGP key pair. 
Save the signing key from
[breakwa11/pubkey](https://github.com/breakwa11/pubkey) as a text file. 
Then do **File** > **Import Certificates** to import the signing key text file.
After import, select the signing key and do 
**Certificates** > **Certify Certificates**. 
You will need to enter the passphrase for your own key. 
Finally, do **File** > **Decrypt/Verify Files** for the executable 
you propose to use (see below). A message confirming successful verification 
of the signature appears against a green background. 
Close program **Kleopatra**.

For >= Windows 8 or with .Net 4.0, using ShadowsocksR-dotnet4.0.exe.

For <= Windows 7 or with .Net 2.0, using ShadowsocksR-dotnet2.0.exe.

#### Usage

1. Find ShadowsocksR icon in the notification tray
2. You can add multiple servers in servers menu
3. Select Enable System Proxy menu to enable system proxy. Please disable other
proxy addons in your browser, or set them to use system proxy
4. You can also configure your browser proxy manually if you don't want to enable
system proxy. Set Socks5 or HTTP proxy to 127.0.0.1:1080. You can change this
port in Global settings
5. You can change PAC rules by editing the PAC file. When you save the PAC file
with any editor, ShadowsocksR will notify browsers about the change automatically
6. You can also update the PAC file from GFWList. Note your modifications to the PAC
file will be lost. However you can put your rules in the user rule file for GFWList.
Don't forget to update from GFWList again after you've edited the user rule
7. For UDP, you need to use SocksCap or ProxyCap to force programs you want
to proxy to tunnel over ShadowsocksR

### Develop

Visual Studio Express 2012 is recommended.

#### License

GPLv3

Copyright © BreakWa11 2017. Fork from Shadowsocks by clowwindy

[Appveyor]:       https://ci.appveyor.com/project/breakwa11/shadowsocksr-csharp
[Build Status]:   https://ci.appveyor.com/api/projects/status/itcxnad1y95gf2x5/branch/master?svg=true
[latest release]: https://github.com/shadowsocksr/shadowsocksr-csharp/releases


下載到最新版4.7.0之後，你會發現它是一個7zip檔案，你的電腦需要有7zip或WinRAR才可為它解壓縮（如果你的WinRAR解壓不到，請安裝7zip，下載網址：http://www.7-zip.org）。

Step1：取得資源的設定檔（如有）

除了手動輸入伺服器資料外，ShadowsocksR還支援匯入設定檔，這樣就毋須逐項資料打進去。在筆者使用的SSR資源中，就有提供設定檔。（如果你找到的資源沒有提供設定檔，請繼續看下去，以手動輸入資料）





Step2：打開ShadowsocksR讀入設定檔 或 手動輸入伺服器資料

解壓縮下載得來的ShadowsocksR後，直接執行它裡面的ShadowsocksR-dotnet4.exe檔案。



你會在電腦畫面右下角Windows系統列中找到ShadowsocksR的圖示。請以滑鼠右擊此圖示，並進入「伺服器＞從文件導入伺服器」，再讀入剛才下載得來的json設定檔便可。



如果伺服器資源沒有設定檔提供，就直接點擊ShadowsocksR在Windows系統列的圖示，在彈出來的「編輯伺服器」視窗中手動輸入資料，包括伺服器網址、連接埠、密碼、加密方式、協議、混淆方式等。



Step3：選取使用你新增的伺服器

利用滑鼠右擊ShadowsocksR的Windows系統列圖示，進入「伺服器」，並選取你剛才加入的伺服器。



Step4：選取使用「全局模式」，開始上網！

最後同樣在ShadowsocksR的選單中，進入「系統代理模式」，選擇「全局模式」便正式使用SSR來翻牆上網。在此選項中選擇「直連模式」或者將ShadowsocksR結束，就能回復正常的上網狀態。
