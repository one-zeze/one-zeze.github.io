---
title: Journey Genie (2023.03 ~ 2023.04)
permalink: /journeygenie/
share: false
related: false
toc: true
toc_sticky: true
toc_label: "Journey Genie"
toc_icon: "laptop-code"
---

## Description

팀 프로젝트  
Team - 프론트 3, 백엔드 3  
Position - 팀 리더, 백엔드 개발  
**[GitHub - JourneyGenie](https://github.com/one-zeze/JourneyGenie)**  
<br>
국비교육 과정 프로젝트로, 약 한 달간 간단한 프로토타입 수준의 애플리케이션 개발  
문서(개발 일정표, 프로젝트 제안서, 설계 명세서, Diagram 등) 작성, DB 설계, Open API 연동, 전반적인 백엔드 개발 수행함.

#### Destination

기차와 (고속/시외)버스의 예매 및 운행정보를 한 화면에서 확인할 수 있는 웹 서비스.  
특정 목적지까지 가기 위해, 기차 탑승 후 시외버스로 환승을 해야 할 때, 기차와
버스의 운행정보를 각각 번갈아가며 확인해야 하는 번거로움을 해결하는 것을 목표로 함.
<br>

## Stack

**IDE** :  
<img src="https://img.shields.io/badge/Intelij-white?style=flat&logo=intellijidea&logoColor=000000">
<img src="https://img.shields.io/badge/Visual_Studio_Code-white?style=flat&logo=visualstudiocode&logoColor=007ACC">

**Back** :  
<img src="https://img.shields.io/badge/Spring_Boot_3.0.4-white?style=flat&logo=springboot&logoColor=6DB33F">
<img src="https://img.shields.io/badge/JDK_17-white?style=flat&logo=openjdk&logoColor=000000">  
<img src="https://img.shields.io/badge/JPA_Hibernate-white?style=flat&logo=hibernate&logoColor=59666C">
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white">

**Front** :  
<img src="https://img.shields.io/badge/HTML5-E34F26.svg?style=flat&logo=html5&logoColor=white">
<img src="https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white">
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=white">
<img src="https://img.shields.io/badge/Thymeleaf-white?style=flat&logo=thymeleaf&logoColor=005F0F">

**협업** :  
<img src="https://img.shields.io/badge/TortoiseSVN-blue?style=flat">
<img src="https://img.shields.io/badge/Notion-white?style=flat&logo=notion&logoColor=000000">
<img src="https://img.shields.io/badge/Discord-5865F2?style=flat&logo=discord&logoColor=white">
<br>

## Develope Log

**기차, 고속/시외 버스 운행정보 조회**

- [공공데이터포털](https://www.data.go.kr/) 오픈 API 사용
- 변동 사항이 적은 기차역과 터미널 정보는 DB 저장하여 사용, 운행정보는 오픈 API를 호출하여 제공하도록 함
- 출발지/도착지에 값이 입력되면, 자동으로 해당 노선의 운행정보 조회하는 기능 구현.

**예매(발권 및 결제)**

- 실제 결제까지는 진행되지 않고, 예매하려는 운행정보를 저장하도록 구현함. (사업자등록, PG 계약 문제)로 결제 기능 미구현.

**회원가입/로그인**

- 회원가입 진행 시, 입력된 정보가 DB에 중복되는지 검증하는 기능 구현.
- 로그인 시 회원의 특정 값을 HttpSession을 통해 클라이언트에게 전달하고, 내부 api 호출 시 해당 값을 사용해 회원정보를 구분할 수 있게 구현함.

**API 통합/테스트**

- Ajax 사용하여, 프론트와 내부 spring 서버 연결 및 테스트 수행

**Etc**

- 전반적으로 1:N, N:1과 같이 양방향으로 매핑된 Entity 객체를 출력할 때, 순환 참조(toString() 함수로 인한 StackOverFlow)가 발생하는 것을 확인함. Entity 객체를 DTO, VO 객체로 변환 후에 전달하도록 하여 해결함.

<br>

## Contribution

-- 서비스의 핵심 기능에 높은 우선순위를 두자는 의견을 팀원들과 공유하여, 보다 높은 완성도를 달성하는 데에 기여함  
-- 효율적인 협업과 진행을 위해 주간/일일 회의 진행  
-- 프로젝트의 전체적인 작업 일정표와 각 팀원별로 단위작업 일정표 작성하여 공지
