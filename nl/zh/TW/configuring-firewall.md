---

copyright:
  years: 2017
lastupdated: "2018-11-12"

keywords: configure, configuring, firewall, add, adding, edit, editing, rules, ports, common

subcollection: hardware-firewall-shared

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}
{:note: .note}
{:important: .important}

# 配置 Hardware Firewall
{: #configuring-the-hardware-firewall-shared-}

配置防火牆與建立一組規則一樣簡單，以容許從特定的網際網路位址存取特定 IP 位址/埠，同時拒絕來自其他來源的資料流量。

## 將防火牆新增至伺服器
{: #adding-a-firewall-to-a-server}

若要將防火牆新增至伺服器中，請遵循[開始使用](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-getting-started-with-hardware-firewall-shared)中的步驟。若收到錯誤，請參閱[已知限制](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-known-limitations-with-hardware-firewall-shared-)，以及（或）聯絡 SoftLayer 支援人員。

## 編輯規則
{: #editing-rules}

首次將防火牆新增至伺服器時，一開始會準備好一組規則，以容許所有資料流量到達伺服器。然後可以編輯規則來控製到達伺服器的資料流量。

確定「狀態」會指出防火牆為「處理所有規則」。若實作的規則對使用者的環境具有非預期的影響，使用者可以按一下**動作**下拉清單中的**略過規則**，來選擇略過規則。

1. 從瀏覽器中，開啟[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/){: new_window} 並登入您的帳戶。
2. 在「客戶入口網站」導覽中，移至**裝置 > 裝置清單**，然後按一下您要配置的防火牆受保護裝置。
3. 在**防火牆**標籤中，確定「狀態」會指出防火牆為「處理所有規則」。該頁面會顯示對 IPv4 和 IPv6 位址生效的現行規則。若未實作任何規則，則會顯示模糊的位置保留元。此時，鏈結可用於編輯現行規則。此規則清單稱為「工作配置」。「工作配置」是一組正在建立但尚未套用至防火牆的規則。使用者可以編輯、新增及刪除規則，直到完成規則集為止。

     規則會以其處理的順序來顯示，編號較小的規則優先於編號較高的規則（如果規則一允許封包通過，則該封包會忽略規則二及之後的規則）。

     欄位如下：

      **順序** - 此欄位包含規則號碼。可以使用提供的箭頭在清單中向上或向下移動規則。

      **動作** - 此選取清單用於「允許」或「拒絕」符合此規則的資料流量。

      **來源** - 此欄位可以是「任何」或特定的 IP 位址，也可以是特定子網路的網址。

      **目的地** - 此欄位會選取目的地 IP（若有問題，請參閱[已知限制](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-known-limitations-with-hardware-firewall-shared-)）。

      **CIDR** - 此欄位表示所選來源/目的地的標準 CIDR 表示法。

      **埠範圍** - 這兩個欄位表示規則將套用至其中的埠範圍（介於 1 和 65535 之間）。

      **通訊協定** - 此欄位會選取規則將套用至其中的通訊協定 (TCP/GRE/ICMP/UDP/PPTP/AH/ESP)。

      **附註：** 開放式欄位，可以輸入此規則的任何相關附註。

4. 按一下規則以進行編輯，或按一下表格底端的加號以新增其他規則。按一下減號圖示會刪除規則。規則會在您輸入時自動進行驗證。

5. 「工作配置」完成之後，請按**更新規則**按鈕，以讓「工作配置」套用至防火牆。規則應在兩分鐘內生效。

## 共用埠
{: #common-ports}

|通訊協定 |埠 |
| :-----: | :-----: |
|FTP |21 |
|SSH |22 |
|Telnet |23 |
|SMTP |25 |
|DNS |53 |
|HTTP |80 |
|POP3 |110 |
|IMAP |143 |
|HTTPS |443 |
|MSSQL |1433 |
|MySQL |3306 |
|遠端桌面 |3389 |
|PostgreSQL |5432 |
|VNC Web |5800 |
|VNC 用戶端 |5900 |
|Urchin |9999 或 10000 ||
