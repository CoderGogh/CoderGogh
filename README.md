<h1 align="center">Hi 👋, I'm CoderGogh</h1>
<h3 align="center">Backend Developer focused on Scalability & Data Processing</h3>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com/?lines=Spring+Backend+Developer;Batch+Processing+Engineer;Distributed+System+Enthusiast;Data+%2B+AI+Driven+Thinking&center=true&width=500&height=50">
</p>

---

## 🧑‍💻 About Me

- 📌 **대용량 데이터 처리와 백엔드 아키텍처에 관심 있는 개발자**
- ⚙️ **Spring 기반 서버 / 배치 / 메시징 시스템 경험**
- 🧠 **AI + 데이터 기반 문제 해결 경험**
- 🎯 목표: **확장 가능한 시스템을 설계하는 백엔드 엔지니어**

---

## 🛠️ Tech Stack

### Backend
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Spring](https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![SpringBoot](https://img.shields.io/badge/SpringBoot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)

### Data & Infra
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![ElasticSearch](https://img.shields.io/badge/ElasticSearch-005571?style=for-the-badge&logo=elasticsearch&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)

### Messaging / Batch
![Kafka](https://img.shields.io/badge/Kafka-000000?style=for-the-badge&logo=apachekafka)
![SpringBatch](https://img.shields.io/badge/SpringBatch-6DB33F?style=for-the-badge)

### DevOps
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws)

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=CoderGogh&show_icons=true&theme=tokyonight&hide_border=true"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=CoderGogh&layout=compact&theme=tokyonight&hide_border=true"/>
</p>

---

# 🚀 Projects

---

## 🏗️ 1. 대규모 배치 & 메시지 전송 플랫폼

> **"100만 유저 / 500만 건 데이터 정산 + Kafka 기반 비동기 메시징 시스템"**

### 🔥 문제
- 대규모 데이터 정산 시 **정확성과 성능을 동시에 확보 필요**
- 동기 처리 구조에서는 **속도 한계 발생**

### ⚙️ 해결
- **Spring Batch 기반 정산 시스템 설계**
- **Kafka 기반 비동기 메시징 구조 도입**
- ACK/NACK 기반 재전송 로직 구현
- Redis 캐싱으로 DB 부하 감소

### 🧠 핵심 설계
- 정산: **정확성 중심**
- 메시징: **속도 중심 (모듈 분리)**
- 재시도 3회 + 실패 대응 구조

### 📈 성과
- **500만 건 데이터 안정적 처리**
- 배치 + 메시징 분리로 **확장성 확보**
- 운영자 UI (진행률 / 로그 시각화) 설계

### 🛠️ Tech
Spring Boot, Spring Batch, Kafka, Redis, MySQL, Docker, AWS EC2

---

## 🤖 2. 고객 상담 분석 & AI 기반 리포트 시스템

> **"AI + ElasticSearch 기반 상담 데이터 분석 플랫폼"**

### 🔥 문제
- 상담 데이터가 **비정형 텍스트 → 분석 어려움**
- 검색 기능이 단순 키워드 수준

### ⚙️ 해결
- **AI API(Gemini)로 상담 요약 및 분석**
- MongoDB에 **역정규화 데이터 저장**
- ElasticSearch로 **검색 + 키워드 집계**

### 🧠 핵심 설계
- 분석용 / 검색용 인덱스 분리
- Redis 캐시 활용
- AI 기반 상담 품질 평가 로직

### 📈 성과
- 상담 데이터 → **분석 리포트 자동 생성**
- 키워드 기반 추천 검색 구현
- 상담 품질 평가 자동화

### 🛠️ Tech
Spring Boot, ElasticSearch, MongoDB, Redis, AWS S3, Docker, AI API

---

## ⚡ 3. 전기차 충전소 통합 정보 시스템

> **"외부 API 호출 최적화 + 공간 데이터 처리 시스템"**

### 🔥 문제
- 외부 API 호출 과다 → **성능 저하**
- 사용자 증가 시 지연 발생

### ⚙️ 해결
- **반경 기반 필터링으로 API 호출 제한**
- Redis 캐싱 적용
- PostGIS 활용한 공간 데이터 처리

### 📈 성과
- API 호출 횟수 감소
- 성능 병목 구간 분석 경험
- 트래픽 증가 시 구조 개선 필요성 인식

### 🛠️ Tech
FastAPI, PostgreSQL, PostGIS, Redis, JWT

---

## 🌐 4. SNS 서비스 (Spring 기반)

> **"Spring Security 기반 인증/인가 시스템 구축"**

### 🔥 문제
- 인증 구조 단순 → 보안 확장 필요

### ⚙️ 해결
- Spring Security 기반 인증 시스템
- 쿠키 기반 로그인 구조 설계
- GCS 활용 이미지 저장

### 📈 성과
- 서버 사이드 렌더링 구조 경험
- 인증/보안 설계 이해

### 🛠️ Tech
Spring Boot, Spring Security, Thymeleaf, MySQL, GCS

---

## 🧪 5. Twitter Clone (대학교 프로젝트)

> **"검색 UX 개선 경험 → 자연어 검색으로 확장"**

### 🔥 문제
- 해시태그 기반 검색 → 사용자 불편

### 💡 인사이트
- 자연어 기반 검색 필요성 인식
- 이후 프로젝트에서 ElasticSearch 적용으로 발전

### 📈 성과
- RDB 설계 및 데이터 정합성 이해
- NLP/검색 시스템에 대한 관심 확장

---

## 🧠 6. 딥러닝 심화 학습

- PyTorch 기반 모델 학습
- 모델 성능 개선 실습
- 논문 분석 및 발표 경험

👉 **검색/추천 시스템으로 관심 확장**

---

## 📈 Activity Graph

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=CoderGogh&theme=tokyo-night&hide_border=true"/>
</p>

---

## 🐍 Contribution Snake

<p align="center">
  <img src="https://raw.githubusercontent.com/CoderGogh/CoderGogh/output/github-contribution-grid-snake.svg" />
</p>

---

## 📫 Contact

- Email: your-email@example.com
- Blog: https://your-blog.com

---

⭐️ From https://github.com/CoderGogh
