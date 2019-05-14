綠界科技 OpenCart 模組
===============
<p align="center">
<img src="https://img.shields.io/github/release/ECPay/OpenCart3.0.svg" alt="Last Release">
</p>

提供合作特店以及個人會員使用開放原始碼商店系統時，無須自行處理複雜的檢核，直接透過安裝設定外掛套件，便可以較快速的方式介接綠界系統。


目錄
-----------------
* [支援版本](#支援版本)
* [安裝](#安裝)
* [設定](#設定)
	1. [金流](#金流)
	2. [電子發票](#電子發票)
	3. [物流](#物流)
* [技術支援](#技術支援)



支援版本
-----------------
| OpenCart  | 模組 |
| :---------: | :----------: |
|  3.0.2.0 | 3.0.190410 |
 

安裝
-----------------
####環境需求
請確認已安裝 PHP `curl` 模組。
安裝與設定: https://www.php.net/manual/en/curl.installation.php

####上傳模組
`購物車後台` -> `擴充功能` -> `擴充安裝`，上傳 ecpaypayment.ocmod.zip。

#### 更新 OCMOD
`購物車後台` -> `擴充功能` -> `修改設定` -> 點擊右上角更新按鈕。

設定
-----------------

#### 金流

**啟用**
- `購物車後台` -> `擴充功能` -> `支付模組` -> `綠界整合金流`，點選右邊`新增`按鈕。
- `購物車後台` -> `擴充功能` -> `支付模組` -> `綠界整合金流`，點選右邊 `編輯` 按鈕。
- 至 [綠界管理後台](https://vendor.ecpay.com.tw/)，查詢以下資訊並回填。

|  購物車後台欄位名稱 | 綠界管理後台欄位名稱  |
| :------------: | :------------: |
|  商店代號 | 商店代號 |
|  金鑰 |  介接 HashKey |
|  向量 |  介接 HashIV |

**注意事項**
- 請注意 Hash Key 與 Hash IV內容不可包含空白。
- 商店代號 `2000132` 為測試代號，請勿使用於正式營運環境。
- 建議使用複製 + 貼上回填資訊
- 將狀態設為`啟用`，其他選項請依需求設定*(信用卡分期功能僅適用於特約商店)*，按下`儲存`完成設定。

#### 電子發票
**啟用**
- `購物車後台` -> `擴充功能` -> `支付模組` -> `綠界電子發票`，點選右邊`新增`按鈕。
- `購物車後台` -> `擴充功能` -> `支付模組` -> `綠界整合金流`，點選右邊 `編輯` 按鈕。
- 至 [綠界管理後台](https://vendor.ecpay.com.tw/)，查詢以下資訊並回填。

|  購物車後台欄位名稱 | 綠界管理後台欄位名稱  |
| :------------: | :------------: |
|  商店代號 | 商店代號 |
|  金鑰 |  介接 HashKey |
|  向量 |  介接 HashIV |

**手動開立**
- `購物車後台` -> `銷售統計` -> `訂單管理` -> `訂單清單`，點選右邊 `電子發票` 按鈕。

**注意事項**
- 開立發票網址，預設為測試用網址，請勿使用於正式營運環境。
- 請注意 Hash Key 與 Hash IV內容不可包含空白。
- 自動開立，請將 自動開立電子發票狀態設為 `啟用` 。
- 將狀態設為 `啟用`， 按下 `儲存`完成設定。
- 須使用綠界整合金流，付款方式才能使用此功能

#### 物流
**啟用**
- `購物車後台` -> `擴充功能` -> `運送模組` -> `綠界超商取貨付款`，點選右邊`新增`按鈕。
- `購物車後台` -> `擴充功能` -> `運送模組` -> `綠界超商取貨付款`，點選右邊 `編輯` 按鈕。
- 至 [綠界管理後台](https://vendor.ecpay.com.tw/)，查詢以下資訊並回填。

|  購物車後台欄位名稱 | 綠界管理後台欄位名稱  |
| :------------: | :------------: |
|  商店代號 | 商店代號 |
|  金鑰 |  介接 HashKey |
|  向量 |  介接 HashIV |

**參數設定**
- 請根據您的申請資料輸入必要參數，1.商店代號(Merchant ID)、2.金鑰(Hash Key) 、3.向量(Hash IV) ，並設定各運送方式的運費及狀態，最後再將一般設定的狀態改成啟用。

**變更門市**
- `購物車後台` -> `銷售統計` -> `訂單管理` -> `訂單清單` -> `運送地址`，點選下方 `變更門市` 按鈕。

**建立物流訂單**
- `購物車後台` -> `銷售統計` -> `訂單管理` -> `訂單清單` -> `運送方式`，點選右邊 `建立物流訂單` 按鈕。

**注意事項**
- 綠界超商取貨付款套件安裝完成後，上述參數會帶入測試帳號為預設值，若您尚未取得廠商專屬帳號，請致電綠界科技，請勿使用於正式營運環境。
- 請注意 Hash Key 與 Hash IV內容不可包含空白。
- 須使用綠界整合金流、綠界超商取貨付款，其中一種付款方式才能使用此功能

技術支援
-----------------
綠界技術客服信箱: techsupport@ecpay.com.tw
