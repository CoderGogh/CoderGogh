<p align="center"> <img src="https://capsule-render.vercel.app/api?type=waving&color=58A6FF&height=200&section=header&text=CoderGogh&fontSize=50&fontColor=ffffff"/> </p>

<p align="center">
  <img src="./typing-cursor.svg" width="500" height="160" alt="Backend Engineer / Kafka + Spring Batch / Elasticsearch + Data Pipelines">
</p>

---

## About

  **Hi there👋🏻, I'm Haram Jeong — Backend Developer.**<br>
 I build data-intensive backend systems: batch pipelines, event-driven messaging, and search infrastructure.

 I've led three projects end-to-end, usually owning the data flow design, recovery logic, and failure handling — not just the feature itself:

- **Settlement batch** — Kafka-based pipeline handling 5M+ daily transactions
- **AI-assisted CRM** — consultation summary, search & analytics system
- **EON** — geospatial EV charging platform built on PostGIS (IITP 원장상)

| | |
|:---|:---|
| <img src="https://skillicons.dev/icons?i=kafka" width="22" /> &nbsp;**Messaging & Batch** | Kafka, Spring Batch, chunk processing, Producer-side retry |
| <img src="https://skillicons.dev/icons?i=elasticsearch" width="22" /> &nbsp;**Search & Data** | Elasticsearch, Nori, MongoDB, CQRS |
| <img src="https://skillicons.dev/icons?i=spring" width="22" /> &nbsp;**Backend** | Java, Spring Boot, JPA/JDBC, FastAPI, PostgreSQL/PostGIS |
| <img src="https://skillicons.dev/icons?i=docker" width="22" /> &nbsp;**Ops** | Redis caching, Docker, AWS |

---

## Stack

<table>
  <tr>
    <td><b>Backend</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=java" />
      <img src="https://skillicons.dev/icons?i=spring" />
      <img src="https://skillicons.dev/icons?i=hibernate" />
    </td>
  </tr>
  <tr>
    <td><b>DB & Messaging</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=mysql" />
      <img src="https://skillicons.dev/icons?i=mongodb" />
      <img src="https://skillicons.dev/icons?i=postgres" />
      <img src="https://skillicons.dev/icons?i=redis" />
      <img src="https://skillicons.dev/icons?i=kafka" />
    </td>
  </tr>
  <tr>
    <td><b>AI & Search</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=elasticsearch" />
      <img src="https://img.shields.io/badge/Gemini_API-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white" height="48" />
      <img src="https://img.shields.io/badge/Nori-00A98F?style=for-the-badge" height="48" />
    </td>
  </tr>
  <tr>
    <td><b>Infra</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=aws" />
      <img src="https://skillicons.dev/icons?i=docker" />
    </td>
  </tr>
</table>

---

## Main Projects

### AI-based CRM — 상담관리
  #### *2026.02–2026.03 · 7 weeks · 프로젝트 팀장 (BE 6 · FE 1)*

 상담 이력을 Gemini로 자동 요약·분류·품질평가하고, 우수/유사 상담사례 검색과 리포트를 제공하는 상담 관리 플랫폼.

**핵심 기능**
- 상담 이력 AI 자동 요약·분류·품질평가, 우수 상담사례 선정
- 전문/유사 상담사례 검색
- 월/주/일별 리포트 + 관리자·상담사 대시보드

**성과**
- 카테고리별 프롬프트 분기 + 모델 교체(Gemini 2.5 Flash-Lite) → 분류 정확도 60%→85%, 호출 지연 1.2s→0.7s, 비용 80% 절감, 처리량 5.2배
- Elasticsearch + Nori 튜닝 → MySQL Like 대비 검색 속도 80% 단축, 검색 정확도 70% 개선
- CQRS 읽기/쓰기 분리 + DB 상태테이블 아웃박스 패턴 → ES 자원 경합 해소 · 분산 연동 안정성 확보

<p>
  <img src="https://skillicons.dev/icons?i=java" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=spring" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=elasticsearch" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=mongodb" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=redis" width="32" style="margin-right:10px" />
  <img src="https://img.shields.io/badge/Gemini_API-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white" height="26" />
</p>

[repo →](https://github.com/4Ureca)

---

### Async Settlement System — 정산
  #### *2026.01 · 2 weeks · 프로젝트 팀장 (BE 6)*

 일 500만 건 규모의 통신요금 정산 배치와 알림 발송을 Kafka로 비동기 분리한 대용량 파이프라인.

**핵심 기능**
- 대용량 정산 배치 처리 (500만 건/일)
- 이용자 맞춤형 알림 발송 (SMS · Email)
- 실시간 배치 모니터링 대시보드

**성과**
- Kafka로 정산–알림 모듈 이벤트 기반 비동기 연동 → 모듈 결합도 감소
- Kafka 재처리 책임을 Producer로 재설계 → 정산/메시지 유실률 0%
- JPA→JDBC 전환 + Bulk Insert 튜닝 → 배치 처리시간 48% 단축, JVM 로컬 Map 캐시로 반복 DB 조회 제거

<p>
  <img src="https://skillicons.dev/icons?i=java" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=spring" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=kafka" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=mysql" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=docker" width="32" />
</p>

[repo →](https://github.com/urecaProjectTeam2/Ureka_plus)

---

### EON — EV Charging Platform
  #### *2025.08–2025.10 · 9 weeks · 프로젝트 팀장, 백엔드 단독 (현직 FE·PM 각 1)*

🏆 **정보통신기획평가원(IITP) 원장상 · 2025.12**

 정부·성남시 전기차 보조금과 위치 기반 충전소 정보를 한 서비스로 통합해, 실구매가와 주변 충전소를 한 번에 확인.

**핵심 기능**
- 정부/성남시 전기차 보조금 조회
- 위치 기반 충전소·충전기 정보 제공

**성과**
- PostGIS(ST_DWithin · ST_Distance) 반경 매핑 → 조회 사각지대 해소
- 좌표 반올림 캐시 키 + Redis Sorted Set 계층형 캐싱 → 캐시 히트율 40%p 개선, KEPCO 공공 API 의존도 감소
- Redis 계층형 캐싱 후 부하테스트 → RPS 0 → 50~60, 응답 지연 100s → 10ms대 (Locust)
- Group By + ANY(:ids) 배치 쿼리 → N+1 쿼리 방지

<p>
  <img src="https://skillicons.dev/icons?i=python" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=fastapi" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=postgres" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=redis" width="32" style="margin-right:6px" />
  <img src="https://skillicons.dev/icons?i=docker" width="32" />
</p>

[repo →](https://github.com/Get-Your-Eon/Backend_Server)

---

## GitHub Stats

<table align="center">
  <tr>
    <td align="center" style="border: none;">
      <img src="https://github-stats-alpha.vercel.app/api?username=CoderGogh&cc=22272e&tc=79c0ff&ic=79c0ff&bc=00000000" alt="GitHub Stats" height="170" />
    </td>
    <td align="center" style="border: none;">
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=CoderGogh&background=22272e&currStreakNum=79c0ff&sideNums=79c0ff&sideLabels=79c0ff&dates=79c0ff&fire=79c0ff&stroke=00000000&hide_border=true" alt="GitHub Streak" height="170" />
    </td>
  </tr>
</table>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=CoderGogh&theme=tokyo-night&hide_border=true" alt="Activity Graph" />
</p>

![Metrics](./github-metrics.svg)
