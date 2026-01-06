# CVEXPERT
<img width="1200" height="672" alt="image" src="https://github.com/user-attachments/assets/1455e704-95ea-4291-9c34-9e87f41f44fa" />

<br>

<div align="center">

[![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=next.js&logoColor=white)](https://nextjs.org/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=springboot&logoColor=white)](https://spring.io/projects/spring-boot)
[![Keycloak](https://img.shields.io/badge/Keycloak-4D4D4D?style=flat&logo=keycloak&logoColor=white)](https://www.keycloak.org/)
[![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat&logo=terraform&logoColor=white)](https://www.terraform.io/)
[![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white)](https://aws.amazon.com/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)](https://www.docker.com/)

</div>

---

## 팀원 소개

<div align="left">

<!-- TODO: 팀원 정보/깃허브로 교체 -->
<table width="100%">
  <tr>
    <td align="center" width="20%">
      <img src="https://github.com/dlacowns21.png" width="120" height="120" style="border-radius:50%;"/><br/>
      <b>임채준 </b><br/>
      <sub>PM / Infra </sub><br/>
      <sub><a href="https://github.com/dlacowns21">@dlacowns21</a></sub>
    </td>
    <td align="center" width="20%">
      <img src="https://github.com/jihwan77.png" width="120" height="120" style="border-radius:50%;"/><br/>
      <b>황지환 </b><br/>
      <sub>PL / Infra </sub><br/>
      <sub><a href="https://github.com/jihwan77">@jihwan77</a></sub>
    </td>
    <td align="center" width="20%">
      <img src="https://github.com/moonstone0514.png" width="120" height="120" style="border-radius:50%;"/><br/>
      <b>김문석 </b><br/>
      <sub>Infra </sub><br/>
      <sub><a href="https://github.com/moonstone0514">@moonstone0514</a></sub>
    </td>
    <td align="center" width="20%">
      <img src="https://github.com/Minkyoungg0.png" width="120" height="120" style="border-radius:50%;"/><br/>
      <b>문민경 </b><br/>
      <sub>FE / BE</sub><br/>
      <sub><a href="https://github.com/Minkyoungg0">@Minkyoungg0</a></sub>
    </td>
    <td align="center" width="20%">
      <img src="https://github.com/yeomyeoung.png" width="120" height="120" style="border-radius:50%;"/><br/>
      <b>박여명</b><br/>
      <sub>FE / BE</sub><br/>
      <sub><a href="https://github.com/yeomyeoung">@yeomyeoung</a></sub>
    </td>
    
  </tr>
</table>

---


## 목차

1. [프로젝트 개요](#-프로젝트-개요)
2. [시스템 아키텍처](#️-시스템-아키텍처)
3. [주요 서비스 기능](#-주요-서비스-기능)
4. [인프라 및 기술적 특징](#️-인프라-및-기술적-특징)
5. [기술 스택](#️-기술-스택)
6. [트러블슈팅](#-트러블슈팅)
7. [팀원 소개](#-팀원-소개)
8. [리포지토리 링크](#-리포지토리-링크)

---

## 기획 배경 - 문제 상황

#### 1. 취약점 정보는 공개되어 있지만, 실제 실습으로 이어지기 어려움
CVE, 보안 공지, 공격 기법 정보는 충분히 공개되어 있으나,
이를 실제 환경에서 재현하고 검증해볼 수 있는 실습 환경은 제한적입니다.

#### 2. 실습 환경 구축 비용과 복잡도가 학습의 진입 장벽으로 작용
기존 보안 학습은 서버 구성, 네트워크 설정, 취약 환경 구축을
사용자가 직접 수행해야 하는 경우가 많아
시간·비용·보안 측면에서 부담이 큽니다.

#### 3. 안전하게 반복 실습할 수 있는 격리 환경이 부족
실제 공격을 재현하려면 완전히 분리된 환경이 필요하지만,
일반적인 학습 환경에서는 이를 안정적으로 제공하기 어렵습니다.

---

## 프로젝트 개요
CVEXPERT는 <b>가상화된 CVE 환경을 실시간으로 자동 생성</b>하고, <b>웹에서 바로 PoC 실습이 가능</b>한 실전형 보안 트레이닝 플랫폼입니다.

이론 중심의 학습이 아닌,
보안 사고와 취약점 대응 경험을 중심으로 학습할 수 있도록 설계된 서비스입니다.

### 핵심 목표
- **탄력적 실습 환경 운영**<br>
CVE 실습 환경의 생성·삭제가 빈번한 특성을 고려해, 트래픽과 리소스 변동에 유연하게 대응 가능한 인프라 구조 설계

- **무중단 서비스 안정성 확보**<br>
실습 서비스 중단이 학습 경험에 직접적인 영향을 미치는 점을 고려하여, 핵심 구성 요소 중심의 고가용성(HA) 아키텍처 구현

- **운영 자동화 기반 관리 효율화**<br>
실습 환경 생성부터 배포·운영까지 전 과정을 자동화하여, 운영자 개입을 최소화하고 운영 리스크 감소

- **현실적인 비용 최적화**<br>
제한된 물리 자원과 예산 조건을 고려해 비용 대비 효율성을 우선한 인프라 설계

---

## 시스템 아키텍처

CVEXPERT는 실습 환경의 탄력적 운영과 비용 효율성을 고려하여,

**기본 서비스는 온프레미스**에 두고 **실습 환경은 AWS에서 확장**하는 **하이브리드 클라우드 아키텍처**를 채택했습니다.

#### - 인프라 아키텍처
<div align="center">
  <img width="1000" height="600" alt="image" src="https://github.com/user-attachments/assets/e2468bce-fb17-49a3-92bf-a424decee682" />
</div>

#### - 네트워크 아키텍처
<div align="center">
  <img width="1000" height="600" alt="image" src="https://github.com/user-attachments/assets/6530000e-2ca1-4291-b9f0-5b4479999781" />
</div>

---

## 인프라 및 기술적 특징

CVEXPERT는 CVE 실습 환경의 빈번한 생성·소멸이라는 서비스 특성을 고려해,
안정성·운영 효율·비용을 균형 있게 만족하는 인프라 아키텍처를 설계했습니다.

### 1️⃣ 탄력적 실습 환경 운영 (Elastic Lab Provisioning)
- **문제:** 실습 요청 시점마다 인프라가 급격히 생성·삭제되는 구조
- **해결:**
  - Terraform Runner 기반 `create/destroy/status` API로 CVE별 템플릿을 자동 실행
  - 실습 환경은 필요 시점에만 동적으로 AWS에서 확장
- **결과:** 트래픽 변동에도 안정적으로 실습 환경 제공

### 2️⃣ 네트워크 격리 및 안정성 (Network Segmentation & Connectivity)
보안 영역을 명확히 분리하면서도, 온프레미스와 클라우드 간 실습 환경을 안정적으로 연동하기 위해 설계했습니다.
- 온프레미스와 AWS를 **Site-to-Site VPN(IPsec)** 으로 연결
- Service / Management / LAB / CI·CD Zone으로 **네트워크 논리적 분리**
- ESXi 기반 vSwitch를 활용한 영역 간 격리<br>

### 3️⃣ 고가용성 (High Availability)
단일 DB 장애로 인해 실습 및 서비스가 중단되는 상황을 방지하고, 트래픽 변동과 노드 장애 상황에서도 서비스가 지속적으로 제공되도록 설계하였습니다.
- **Database**
  - Master–Replica 구조
  - Virtual IP 기반 요청 분산
  - Orchestrator를 통한 자동 장애 감지 및 승격<br>
- **Kubernetes**
  - Master Node 3대 / Worker Node 3대 구성
  - Ingress, HPA, DaemonSet 기반 트래픽 분산 및 자동 확장<br>

### 4️⃣ 운영 자동화 (Automation)
- **IaC**: Terraform 기반 실습 인프라 생성·삭제 자동화
- **CI/CD**: **GitLab → Jenkins → Harbor → ArgoCD** 파이프라인 구성
- **Security**: **Cosign**을 활용한 컨테이너 이미지 서명 및 무결성 검증<br>

---


## 주요 서비스 기능

### 1. CVE 학습
- 이메일 인증 기반 회원가입 후 로그인 된 사용자만 이용 가능
- 이유?
**1-1. CVE 이론**
   
**1-2. 실제 취약점 기반 PoC 실습**
![lab](lab.gif)


![news](news.gif)
![his](his.gif)



| 기능 | 설명 | 화면 예시 |
| :--- | :--- | :--- |
| **🧪 CVE 실습 시작** | CVE 선택 후 “실습 시작” 클릭만으로 취약 환경 자동 생성 및 PoC 가이드 제공 | <img src="TODO" width="200" /> |
| **🖥️ 웹 원격 접속** | Guacamole 기반으로 별도 설치 없이 브라우저에서 실습 환경 접속 | <img src="TODO" width="200" /> |
| **📄 보고서 템플릿 작성** | 실습 완료 후 정해진 템플릿으로 보고서 작성 및 저장 | <img src="TODO" width="200" /> |
| **📚 마이페이지/이력** | 내가 수행한 CVE 실습 이력, 작성 보고서, 결과 확인 | <img src="TODO" width="200" /> |
| **🛡️ 관리자 관제** | 인스턴스 상태/로그/메트릭 관제 및 장애 탐지(알람) | <img src="TODO" width="200" /> |

---

## ☁️ 인프라 및 기술적 특징

CVEXPERT는 CVE 실습 환경의 빈번한 생성·소멸이라는 서비스 특성을 고려해,
안정성·운영 효율·비용을 균형 있게 만족하는 인프라 아키텍처를 설계했습니다.

### 1️⃣ 탄력적 실습 환경 운영 (Elastic Lab Provisioning)
- **문제:** 실습 요청 시점마다 인프라가 급격히 생성·삭제되는 구조
- **해결:**
  - Terraform Runner 기반 `create/destroy/status` API로 CVE별 템플릿을 자동 실행
  - 실습 환경은 필요 시점에만 동적으로 AWS에서 확장
- **결과:** 트래픽 변동에도 안정적으로 실습 환경 제공

### 2️⃣ 네트워크 격리 및 안정성 (Network Segmentation & Connectivity)
- 온프레미스와 AWS를 **Site-to-Site VPN(IPsec)** 으로 연결
- Service / Management / LAB / CI·CD Zone으로 네트워크 논리적 분리
- ESXi 기반 vSwitch를 활용한 영역 간 격리<br>
→ 보안 영역 분리와 실습 환경 연동을 동시에 만족

### 3️⃣ 고가용성 (High Availability)
단일 DB 장애로 인해 실습 및 서비스가 중단되는 상황을 방지하고, 트래픽 변동과 노드 장애 상황에서도 서비스가 지속적으로 제공되도록 설계하였습니다.
- **Database**
  - Master–Replica 구조
  - Virtual IP 기반 요청 분산
  - Orchestrator를 통한 자동 장애 감지 및 승격<br>
- **Kubernetes**
  - Master Node 3대 / Worker Node 3대 구성
  - Ingress, HPA, DaemonSet 기반 트래픽 분산 및 자동 확장<br>

### 4️⃣ 운영 자동화 (Automation)
- **IaC**: Terraform 기반 실습 인프라 생성·삭제 자동화
- **CI/CD**: **GitLab → Jenkins → Harbor → ArgoCD** 파이프라인 구성
- **Security**: **Cosign**을 활용한 컨테이너 이미지 서명 및 무결성 검증<br>

---

## 🛠️ 기술 스택

| 영역 | 기술 스택 |
| :--- | :--- |
| **Frontend** | ![Next.js](https://img.shields.io/badge/-Next.js-000000?logo=next.js&logoColor=white) ![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?logo=typescript&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/-Tailwind-06B6D4?logo=tailwindcss&logoColor=white) |
| **Backend** | ![Java](https://img.shields.io/badge/-Java-007396?logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/-Spring%20Boot-6DB33F?logo=springboot&logoColor=white) ![JPA](https://img.shields.io/badge/-JPA-59666C?logo=hibernate&logoColor=white) ![Spring Security](https://img.shields.io/badge/-Security-6DB33F?logo=springsecurity&logoColor=white) |
| **Auth** | ![Keycloak](https://img.shields.io/badge/-Keycloak-4D4D4D?logo=keycloak&logoColor=white) |
| **Infra / IaC** | ![AWS](https://img.shields.io/badge/-AWS-232F3E?logo=amazonaws&logoColor=white) ![Terraform](https://img.shields.io/badge/-Terraform-7B42BC?logo=terraform&logoColor=white) ![Docker](https://img.shields.io/badge/-Docker-2496ED?logo=docker&logoColor=white) |
| **Remote Access** | TODO: Guacamole, Tomcat, DB(mysql/postgres) |
| **Monitoring** | TODO: CloudWatch / ELK / PLG (Prometheus, Loki, Grafana) |

---

## 🔥 트러블슈팅

<details>
<summary><strong>1️⃣ (예시) Guacamole iframe 연결 / 토큰 발급 문제</strong></summary>

- **문제:** TODO
- **원인:** TODO
- **해결:** TODO (예: AuthToken 발급 → connection 생성 → 최종 URL 조합)
- **결과:** TODO

</details>

<details>
<summary><strong>2️⃣ (예시) Terraform Runner 상태 관리 / 동시성 문제</strong></summary>

- **문제:** TODO
- **원인:** TODO
- **해결:** TODO (예: remote state, lock, uuid 키 전략)
- **결과:** TODO

</details>

<details>
<summary><strong>3️⃣ (예시) 로그/메트릭 수집 누락(CloudWatch Agent/필터 설정)</strong></summary>

- **문제:** TODO
- **원인:** TODO
- **해결:** TODO
- **결과:** TODO

</details>

---

## 🔗 리포지토리 링크

| 영역 | 설명 | 링크 |
| :--- | :--- | :---: |
| 🎨 **Frontend** | • Next.js 기반 사용자 UI<br>• CVE 목록/필터, 실습 시작, 마이페이지 등 | [TODO-frontend](TODO) |
| ⚙️ **Backend** | • Spring Boot 기반 API 서버<br>• 실습 세션 관리, Guacamole 연동, 사용자/보고서 관리 | [TODO-backend](TODO) |
| 🏗️ **Runner / IaC** | • Terraform Runner 서비스 및 CVE 템플릿<br>• infra provisioning 자동화 | [TODO-runner-or-infra](TODO) |
| 📊 **Monitoring** | • (선택) 관제/대시보드 구성(ELK/PLG/CloudWatch) 문서 | [TODO-monitoring](TODO) |
