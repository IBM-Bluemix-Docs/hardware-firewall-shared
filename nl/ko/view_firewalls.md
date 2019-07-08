---

copyright:
  years: 2017
lastupdated: "2018-11-12"

keywords: views, firewalls, overview, vlan,

subcollection: hardware-firewall-shared

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# 다양한 방화벽 보기
{: #viewing-your-various-firewalls}

보호되지 않은 VLAN 뿐만 아니라 계정에서 사용 중인 방화벽 및 연관된 VLAN을 식별할 수 있으며 방화벽 솔루션의 배치를 계획할 수 있습니다.

## VLAN별 방화벽 개요
{: #firewall-overview-by-vlan}

사용자 시스템의 방화벽에 대한 개요를 가져오고 기본 관리를 시작하려면, [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/){: new_window}에서 **네트워크 > IP 관리 > VLAN**으로 이동하십시오.

공용 VLAN만 보려면 **필터** 드롭 다운을 클릭한 후 **기본 라우터**에 대해 `fcr`을 입력하십시오.
{: tip}

각 행은 인프라에 있는 VLAN을 표시합니다. IBM© Cloud는 실제 VLAN 번호와 구성되어 있는 라우터를 나타내는 **VLAN 번호** 및 **기본 라우터** 정보를 자동으로 채웁니다. **이름** 필드를 사용하여 인식 가능한 이름을 정의하십시오.

**게이트웨이/방화벽** 열에는 어떤 Hardware Firewall 보호가 준비되어 있는지에 대한 세부사항이 포함되어 있습니다. 예를 들어,

**방화벽 추가**는 이 VLAN의 서버에 준비된 방화벽이 없음을 표시합니다.

**개별 보호된 서버**는 하나 이상의 서버에서 Hardware Firewall을 활용하고 있으며 Hardware Firewall (Dedicated), FortiGate Security Appliance 또는 네트워크 게이트웨이가 없음을 나타냅니다. VLAN 방화벽과 네트워크 게이트웨이는 개별 보호된 서버가 있는 VLAN에 배치할 수 없습니다.

**Firewall-vlanXXXX.networklayer.com**은 Hardware Firewall (Dedicated) 또는 FortiGate Security Appliance가 준비되어 있음을 나타냅니다. 단 하나의 VLAN 방화벽 또는 네트워크 게이트웨이를 VLAN과 연관시킬 수 있지만, 서버를 공용 VLAN에서 VLAN 방화벽으로 보호하고 사설 네트워크에서 네트워크 게이트웨이와 연관시킬 수 있습니다.

**GatewayName**은 VLAN이 해당 네트워크 게이트웨이와 연관되어 있음을 나타냅니다.

## 개별 보호된 서버 보기
{: #individually-protected-servers-view}

VLAN 화면에서 **게이트웨이/방화벽** 열에 있는 **개별 보호된 서버** 행을 식별하고 연관된 VLAN 번호 링크를 클릭하십시오. 연관된 디바이스를 포함하여 VLAN에 대한 세부사항이 표시됩니다.

여기에서 각 디바이스를 클릭하여 특정 서버에 대해 방화벽이 준비되어 있는지 검토할 수 있습니다.

디바이스를 클릭했으면 구성 탭의 맨 아래로 스크롤하십시오. 추가 기능 섹션에 **방화벽**이 표시되며 **설치됨** 또는 **설치되지 않음** 상태가 함께 표시됩니다. **설치되지 않음**은 이 디바이스에 대한 방화벽이 준비되어 있지 않음을 나타냅니다. **설치됨**은 방화벽이 준비되어 있으며 방화벽 구성을 관리할 수 있는 **방화벽** 탭을 디바이스에서 사용할 수 있음을 나타냅니다.

## 전용 방화벽 보기
{: #dedicated-firewall-view}

VLAN 화면에서 **게이트웨이/방화벽** 열에 있는 **Firewall-vlanXXXX.networklayer.com** 행을 식별하고 해당 방화벽을 클릭하십시오. Hardware Firewall (Dedicated) 또는 FortiGate Security Appliance 중 하나가 표시됩니다. 디바이스 세부사항에는 연관된 라우터, VLAN 및 IPv4/IPv6 서브넷, 해당 VLAN과 연관된 디바이스 및 방화벽을 통하거나 주변으로 트래픽을 라우팅하기 위한 제어가 포함되어 있습니다.

**FortiGate Security Appliance** 디바이스에는 관리 IP, 사용자 이름 및 비밀번호가 포함됩니다.  관리 GUI 또는 SSH 기반 콘솔을 통해 관리가 완료됩니다.

## 네트워크 게이트웨이 보기
{: #network-gateway-view}

VLAN 화면에서 네트워크 게이트웨이 디바이스에 의해 채워진 **게이트웨이/방화벽** 행을 식별하고 해당 네트워크 게이트웨이를 클릭하십시오. 그런 다음 연관된 프론트 엔드(FCR) 및 백엔드(BCR) VLAN과 네트워크 게이트웨이 관리 옵션이 표시되는 인터페이스로 이동합니다.
