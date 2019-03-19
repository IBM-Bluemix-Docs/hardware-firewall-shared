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

# Hardware Firewall (Shared) 정보
{: #about-hardware-firewall-shared-}

Hardware Firewall (Shared)은 서버의 업스트림에 연결된 네트워크 디바이스입니다. 방화벽은 원치 않는 트래픽이 서버에 도달하기 전에 서버에서 트래픽을 차단합니다. Hardware Firewall을 사용하는 경우의 주요 장점은 서버가 '양호한' 트래픽만 처리하고 '잘못된' 트래픽을 처리하는 데 리소스를 낭비하지 않는다는 것입니다. 

Hardware Firewall (Shared)은 다중 테넌트 엔터프라이즈 플랫폼을 활용하여 개별 서버를 보호합니다.  서버와 함께 구매하거나 나중에 추가할 수 있습니다.  VDOM(Virtual Domain) 기술을 통해 가상화된 네트워크 보안을 제공하며 개별적으로 프로비저닝되고 관리되는 가상화된 보안 도메인을 제공합니다.  

여러 명의 고객이 하드웨어와 연관되어 있으므로 방화벽에 장애가 발생하거나 공격을 받는 경우 Hardware Firewall (Shared) 인스턴스를 공유하는 모든 고객이 영향을 받을 수 있습니다. 

서버에 지정되는 기본 및 정적으로 라우팅되는 IP 주소에 대해 최대 79개의 방화벽 규칙을 구성할 수 있습니다. 공유 방화벽에 대한 보고서는 선택한 날짜 범위의 단일 IP 활동을 기반으로 사용 가능합니다.
고객은 SoftLayer 제어 포털(보호된 서버 세부사항 페이지 아래의 방화벽 탭) 및 SoftLayer SLDN API라는 두 가지 방법을 통해 방화벽을 관리할 수 있습니다.

월별 서버 대역폭이 서버 스위치 포트에 기록되므로 Hardware Firewall (Shared)에서 차단한 트래픽은 월별 할당량으로 계산되지 않으며 원치 않는 트래픽에 대해서는 지불할 필요가 없습니다.

## 개요 및 기능

**사용 목적:** 단일 서버 기본 IP 보호

**사용자 인터페이스:** SoftLayer 제어 포털 및 SoftLayer API로 통합됨

**기능:** Stateful 패킷 검사, 진입 방화벽 규칙, IPv4, IPv6, 기본 로깅

**처리량:** 10Mbps, 100Mbps, 1,000Mbps 또는 2,000Mbps 

Hardware Firewall (Shared) 인스턴스의 처리량은 방화벽이 추가되는 서버의 업링크 속도와 일치해야 합니다.
