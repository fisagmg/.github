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
CVEXPERT는 위와 같은 문제를 해결하기 위해 <br>
이론 중심의 학습을 넘어, **실제 보안 사고와 취약점 대응 경험을 중심으로 학습할 수 있도록 설계된 서비스**입니다.<br>
<br>
**가상화된 CVE 취약 환경을 실시간으로 자동 생성**하고,<br>
별도의 환경 구성 없이 **웹에서 즉시 PoC 실습이 가능한 실전형 보안 트레이닝 플랫폼**을 제공합니다.

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

## 기술 스택

| 영역 | 기술 스택 |
| :--- | :--- |
| **Frontend** | ![Next.js](https://img.shields.io/badge/-Next.js-000000?logo=next.js&logoColor=white) ![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?logo=typescript&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/-Tailwind-06B6D4?logo=tailwindcss&logoColor=white) |
| **Backend** | ![Java](https://img.shields.io/badge/-Java-007396?logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/-Spring%20Boot-6DB33F?logo=springboot&logoColor=white) ![JPA](https://img.shields.io/badge/-JPA-59666C?logo=hibernate&logoColor=white) ![Spring Security](https://img.shields.io/badge/-Spring%20Security-6DB33F?logo=springsecurity&logoColor=white) |
| **Auth** | ![Keycloak](https://img.shields.io/badge/-Keycloak-4D4D4D?logo=keycloak&logoColor=white) |
| **Infra / IaC** | ![AWS](https://img.shields.io/badge/-AWS-232F3E?logo=amazonaws&logoColor=white) ![Terraform](https://img.shields.io/badge/-Terraform-7B42BC?logo=terraform&logoColor=white) ![Docker](https://img.shields.io/badge/-Docker-2496ED?logo=docker&logoColor=white) |
| **DevOps** | ![Kubernetes](https://img.shields.io/badge/-Kubernetes-326CE5?logo=kubernetes&logoColor=white) ![GitLab](https://img.shields.io/badge/-GitLab-FCA121?logo=gitlab&logoColor=white) ![Jenkins](https://img.shields.io/badge/-Jenkins-D24939?logo=jenkins&logoColor=white) ![ArgoCD](https://img.shields.io/badge/-ArgoCD-EF7B4D?logo=argo&logoColor=white) ![Harbor](https://img.shields.io/badge/-Harbor-60B932?logo=harbor&logoColor=white) ![Cosign](https://img.shields.io/badge/-Cosign-4285F4?logo=google&logoColor=white) |
| **Remote Access** | ![Apache Guacamole](https://img.shields.io/badge/-Apache%20Guacamole-5A2D81?logo=apache&logoColor=white) ![Apache Tomcat](https://img.shields.io/badge/-Apache%20Tomcat-F8DC75?logo=apachetomcat&logoColor=black) ![MySQL](https://img.shields.io/badge/-MySQL-4479A1?logo=mysql&logoColor=white) |
| **Monitoring** | ![AWS CloudWatch](https://img.shields.io/badge/-CloudWatch-FF9900?logo=amazonaws&logoColor=white) ![Elasticsearch](https://img.shields.io/badge/-Elasticsearch-005571?logo=elasticsearch&logoColor=white) ![Prometheus](https://img.shields.io/badge/-Prometheus-E6522C?logo=prometheus&logoColor=white) ![Grafana](https://img.shields.io/badge/-Grafana-F46800?logo=grafana&logoColor=white) |

---

## 주요 서비스 기능

### **1. CVE 학습**
- 이메일 인증 기반 회원가입 후 로그인 된 사용자만 이용 가능
- 실습 환경의 보안성과 안정성을 확보하고, 사용자별 학습 이력을 체계적으로 관리하기 위해 접근을 제한

#### **1-1. CVE 이론**
<img src="study.gif" alt="study" width="1000" /> <br>
- CVSS 점수, 영향받는 기술 스택, 취약점 개요 등 CVE별 취약점 상세 정보 제공
- 연도, 분야, 환경 기준의 필터링 및 키워드 검색 지원

<br>

#### **1-2. 실제 취약점 기반 PoC 실습**
<img src="lab.gif" alt="lab" width="1000" /> <br>
- 실습 시작 버튼 클릭 시, 해당 CVE가 적용된 전용 가상 머신 환경 자동 생성
- 단계별 실습 가이드를 따라가며 실제 공격 과정을 직접 재현 가능

<br>

### **2. 보고서 작성**
<img src="his.gif" alt="his" width="1000" /> <br>
- 실무에서 활용되는 보안 취약점 보고서 양식 기반 템플릿 제공
- 마이페이지의 ‘작성한 보고서’ 메뉴에서 보고서 재다운로드, 수정 후 재업로드 가능

<br>

### **3. 실시간 CVE 취약점 뉴스**
<img src="news.gif" alt="news" width="1000" /> <br>
- 최신 CVE 및 보안 이슈 관련 뉴스를 플랫폼 내에서 실시간 제공
- 실습 학습과 함께 최신 보안 트렌드 파악까지 한 번에 가능하도록 구성

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

CVEXPERT는 CVE 실습 환경의 빈번한 생성·소멸이라는 서비스 특성을 고려해,<br>
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

## 🔥 주요 트러블슈팅

<details>
<summary><strong>1️⃣ Guacamole iframe 연결 및 AuthToken 발급 문제</strong></summary>

- **문제:**  
  Keycloak 로그인 이후 Guacamole 실습 화면을 iframe으로 로드할 때  
  인증 실패 또는 무한 리다이렉트, 404 오류 발생

- **원인:**  
  - Guacamole의 iframe 접속 방식과 Keycloak OIDC 인증 흐름 불일치  
  - clientId(Base64) 생성 규칙 미준수  
  - AuthToken 재사용으로 인한 세션 만료 문제

- **해결:**  
  - 백엔드에서 Guacamole REST API를 통해 **AuthToken 발급**
  - AuthToken 기반 **Connection 생성**
  - `connectionId + datasource`를 포함한 **표준 Base64 clientId 생성**
  - 접속 시점마다 신규 토큰을 발급하여 iframe URL 동적 조합

- **결과:**  
  별도 클라이언트 설치 없이,  
  **웹 브라우저에서 안정적으로 실습 환경에 접속 가능한 구조 구현**

</details>

<details>
<summary><strong>2️⃣ Terraform Runner 상태 관리 및 동시성 문제</strong></summary>

- **문제:**  
  여러 사용자가 동시에 실습 환경을 요청할 경우  
  Terraform 상태 충돌로 인해 인프라 생성 실패 또는 상태 불일치 발생

- **원인:**  
  - 로컬 state 파일 사용으로 인한 동시 실행 충돌  
  - 실습 환경 간 상태 파일 공유 문제

- **해결:**  
  - **Remote State(S3)** 기반 상태 관리 적용
  - **Lock 메커니즘(DynamoDB)** 을 통한 동시 실행 제어
  - 실습 요청 단위로 **UUID 기반 state key 전략** 적용

- **결과:**  
  다중 사용자 요청 환경에서도  
  **실습 환경을 안정적으로 병렬 생성·삭제할 수 있는 구조 확보**

</details>

<details>
<summary><strong>3️⃣ CloudWatch 로그·메트릭 수집 누락 문제</strong></summary>

- **문제:**  
  CloudWatch 대시보드 및 Alarm에서  
  CPU, 디스크, 로그 데이터가 정상적으로 표시되지 않거나  
  `INSUFFICIENT_DATA` 상태로 고정됨

- **원인:**  
  - CloudWatch Agent 메트릭 차원 설정과  
    Alarm 조회 차원 불일치  
  - 로그 그룹 및 스트림 네이밍 규칙 불일치

- **해결:**  
  - `aggregation_dimensions` 설정을 통해  
    **InstanceId 단위 메트릭 통합 수집**
  - 로그 그룹·스트림 네이밍 규칙을 백엔드 조회 로직과 통일
  - Agent 설정 변경 후 재배포 자동화

- **결과:**  
  실습 환경 및 서비스 인스턴스에 대해  
  **정확한 로그·메트릭 기반 모니터링 및 알람 체계 구축**

</details>

<details>
<summary><strong>3️⃣ Terraform Runner 실습 환경 삭제 실패 및 리소스 잔존 문제</strong></summary>

- **문제:**  
  실습 종료 또는 만료 시 Terraform destroy가 정상적으로 수행되지 않아  
  EC2, 보안 그룹, 네트워크 리소스가 AWS에 잔존하는 문제 발생

- **원인:**  
  - 실습 환경 생성 과정에서 일부 리소스만 생성된 상태로 오류 발생  
  - Terraform state에는 존재하지만 실제 리소스는 불완전한 상태로 남아  
    destroy 시 의존성 오류 발생

- **해결:**  
  - 실습 환경 생성 단계별 상태를 Runner에서 관리하도록 로직 분리
  - 실패 시점 이후 생성된 리소스만 정리하는 **보정용 destroy 플로우** 추가
  - 실습 환경 단위(UUID)로 리소스 태깅하여 수동·자동 정리 모두 가능하도록 설계

- **결과:**  
  실습 환경 생성·삭제 실패 상황에서도  
  **리소스 누수 없이 안정적으로 회수 가능한 운영 구조 확보**

</details>


---

## 🔗 리포지토리 링크

| 영역 | 설명 | 링크 |
| :--- | :--- | :---: |
| 🎨 **Frontend** | • Next.js 기반 사용자 UI<br>• CVE 목록/필터, 실습 시작, 마이페이지 등 | [CVEXPERT-frontend](https://github.com/fisagmg/frontend.git) |
| ⚙️ **Backend** | • Spring Boot 기반 API 서버<br>• 실습 세션 관리, Guacamole 연동, 사용자/보고서 관리 | [CVEXPERT-backend](https://github.com/fisagmg/backend.git) |
| 🏗️ **Runner / IaC** | • Terraform Runner 서비스 및 CVE 템플릿<br>• infra provisioning 자동화 | [CVEXPERT-runner-or-infra](https://github.com/fisagmg/infra.git) |
| 📊 **Monitoring** | • 관제/대시보드 구성(ELK/PLG/CloudWatch) 문서 | [CVEXPERT-monitoring](https://github.com/fisagmg/monitoring.git) |
