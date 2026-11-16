<p align="center"> <img src="https://capsule-render.vercel.app/api?type=waving&color=58A6FF&height=200&section=header&text=CoderGogh&fontSize=50&fontColor=ffffff"/> </p>

<p align="center">
  <img src="./typing-cursor.svg" width="500" height="160" alt="Backend Engineer / Kafka + Spring Batch / Elasticsearch + Data Pipelines">
</p>

<!-- Insights & Skills design based on github.com/rladntlr (originally github.com/rdme0) -->
<a href="https://github.com/CoderGogh">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/github-metrics-dark.png">
    <img src="assets/github-metrics-light.png" width="800" alt="CoderGogh의 GitHub Insights — 지난 1년 입체 기여 그래프, 언어 비율, PR 및 이슈 통계">
  </picture>
</a>

## 🛠️ Skills
<!-- Glass icons: scripts/render_skills.py --fetch --browser-channel chrome -->

### Languages

<p>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/java-glass-dark.png">
    <img src="assets/skills/java-glass-light.png" width="84" alt="Java">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/python-glass-dark.png">
    <img src="assets/skills/python-glass-light.png" width="84" alt="Python">
  </picture>
</p>

### Backend

<p>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/springboot-glass-dark.png">
    <img src="assets/skills/springboot-glass-light.png" width="84" alt="Spring Boot">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/hibernate-glass-dark.png">
    <img src="assets/skills/hibernate-glass-light.png" width="84" alt="JPA">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/fastapi-glass-dark.png">
    <img src="assets/skills/fastapi-glass-light.png" width="84" alt="FastAPI">
  </picture>
</p>

### DB & Messaging

<p>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/mysql-glass-dark.png">
    <img src="assets/skills/mysql-glass-light.png" width="84" alt="MySQL">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/postgresql-glass-dark.png">
    <img src="assets/skills/postgresql-glass-light.png" width="84" alt="PostgreSQL">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/mongodb-glass-dark.png">
    <img src="assets/skills/mongodb-glass-light.png" width="84" alt="MongoDB">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/redis-glass-dark.png">
    <img src="assets/skills/redis-glass-light.png" width="84" alt="Redis">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/kafka-glass-dark.png">
    <img src="assets/skills/kafka-glass-light.png" width="84" alt="Kafka">
  </picture>
</p>

### AI & Search

<p>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/elasticsearch-glass-dark.png">
    <img src="assets/skills/elasticsearch-glass-light.png" width="84" alt="Elasticsearch">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/nori-glass-dark.png">
    <img src="assets/skills/nori-glass-light.png" width="84" alt="Nori">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/gemini-glass-dark.png">
    <img src="assets/skills/gemini-glass-light.png" width="84" alt="Gemini API">
  </picture>
</p>

### Data Pipeline & Infra

<p>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/airflow-glass-dark.png">
    <img src="assets/skills/airflow-glass-light.png" width="84" alt="Airflow">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/githubactions-glass-dark.png">
    <img src="assets/skills/githubactions-glass-light.png" width="84" alt="Actions">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/gitlab-glass-dark.png">
    <img src="assets/skills/gitlab-glass-light.png" width="84" alt="GitLab">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/docker-glass-dark.png">
    <img src="assets/skills/docker-glass-light.png" width="84" alt="Docker">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/skills/aws-glass-dark.png">
    <img src="assets/skills/aws-glass-light.png" width="84" alt="AWS">
  </picture>
</p>

## 💾 Projects

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>💸 <a href="https://github.com/CoderGogh/async-settlement-system">Async Settlement System</a></h3>
      <p>📦 <b>일 500만 건 통신요금 정산</b></p>
      <p>정산 배치와 알림 발송을 Kafka로 비동기 분리했습니다. 재처리 책임을 Producer로 옮겨 유실률 0%를 만들고, JPA→JDBC 전환과 Bulk Insert 튜닝으로 배치 시간을 48% 줄였습니다.</p>
      <p><code>Spring Batch</code> <code>Kafka</code> <code>MySQL</code></p>
      <p><a href="https://async-settlement-system.vercel.app">🚀 deploy</a></p>
    </td>
    <td width="50%" valign="top">
      <h3>🎧 <a href="https://github.com/4Ureca">AI-based CRM</a></h3>
      <p>🤖 <b>Gemini 상담 요약·분류·품질평가</b></p>
      <p>카테고리별 프롬프트 분기와 모델 교체로 분류 정확도를 60%→85%로 올리고 비용을 80% 줄였습니다. Elasticsearch + Nori 튜닝으로 검색 속도를 80% 단축했습니다.</p>
      <p><code>Spring Boot</code> <code>Elasticsearch</code> <code>Gemini API</code></p>
      <p><a href="https://aicc-crm.vercel.app">🚀 deploy</a></p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>⚡ <a href="https://github.com/CoderGogh/Eon-BackEnd-Server">EON</a></h3>
      <p>🏆 <b>정보통신기획평가원(IITP) 원장상</b></p>
      <p>전기차 보조금과 위치 기반 충전소 정보를 하나로 통합했습니다. PostGIS 반경 매핑과 Redis 계층형 캐싱으로 응답 지연을 100s에서 10ms대로 줄였습니다.</p>
      <p><code>FastAPI</code> <code>PostGIS</code> <code>Redis</code></p>
      <p><a href="https://get-your-eon.vercel.app">🚀 deploy</a> · <a href="https://github.com/CoderGogh/Eon-FrontEnd-Server">frontend</a></p>
    </td>
    <td width="50%" valign="top">
      <h3>🗺️ <a href="https://github.com/CoderGogh/seoul-ev-data-platform">Seoul EV Siting Platform</a></h3>
      <p>🔁 <b>Airflow DAG 7개 데이터 파이프라인</b></p>
      <p>EV 등록현황과 실시간 도로소통정보를 주기별로 수집·정제해 행정동 단위로 결합하고, 충전소 우선 검토 지역을 선정합니다. 수집부터 품질 모니터링까지 직접 설계했습니다.</p>
      <p><code>Airflow</code> <code>PostGIS</code> <code>GitLab CI</code></p>
      <p><a href="https://seoul-ev-insight.vercel.app">🚀 deploy</a></p>
    </td>
  </tr>
</table>

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


![Metrics](./github-metrics.svg)
