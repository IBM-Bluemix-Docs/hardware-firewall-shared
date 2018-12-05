---

copyright:
  years: 2017
lastupdated: "2018-11-12"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# 已知限制

Hardware Firewall (Shared) 無法部署到符合下列任何準則的 VLAN 上的伺服器中。 

* 目前與「網路閘道」、Hardware Firewall 或 FortiGate Security Appliance 相關聯。
* 包含 30 台以上的伺服器。
* 具有大於 /28 的主要子網路。

在這些實例中，必須為「防火牆」建立新的 VLAN，或者必須選取另一個產品。

Hardware Firewall (Shared) 的進一步限制包括： 

* 可攜式子網路不受保護
* 不適用於 10Gb 伺服器
* 每個 Hardware Firewall (Shared) 最多有 79 個防火牆規則
* 由於處理 ARP 的方式而與「Windows 網路負載平衡 (NLB)」不相容
