# Laravel 9 管理在來源中的網域名稱轉址，以獲得更好的搜尋引擎優化結果

引入 sirodiaz 的 laravel-redirection 套件來擴增管理在資料庫或其他來源中的網域名稱轉址，以獲得更好的搜尋引擎優化結果，301 狀態碼是永久性轉址，而 302 狀態碼則是暫時性轉址。如果想將舊頁面的搜尋引擎優化分數傳遞給新頁面，並且減少轉址後網頁在 Google 搜尋引擎排名的影響，應該使用 301 狀態碼。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 在瀏覽器中輸入已定義的路由 URL 來訪問，例如：http://127.0.0.1:8000。
- 你可以經由 `/old/welcome` 來轉址到 `/welcome`。

----

## 畫面截圖
![](https://i.imgur.com/hEqD70q.png)
> 雖然使用者通常無法分辨不同的重新導向類型，但 Google 搜尋會將重新導向視為強烈或微弱信號，表示重新導向目標應為標準網址