<p align="">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=TypeScript&logoColor=white"/>
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=Node.js&logoColor=white"/>
  <img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=NestJS&logoColor=white"/>
</p>  

<p align="">
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=MySQL&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-3178C6?style=flat-square&logo=Docker&logoColor=white"/>
</p>

![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=luckyhyom&show_icons=true&theme=gruvbox_light)

# 김효민

- GitHub: https://github.com/luckyhyom
- Blog: https://baejjang.tistory.com
- Email: gyals0386@gmail.com


## 소개

5년차 소프트웨어 개발자. 주로 Node.js/TypeScript 기반 백엔드 개발을 해왔으며, 복잡한 비즈니스 로직 설계와 프로덕션 환경 운영 경험이 있다. 스타트업에서 백엔드 총괄, 태양광 사업 운영 시스템 개발 리드, 차량 S/W 개발까지 다양한 도메인을 경험했다. 팀 내 문서화와 프로세스 개선에 적극적이며, 기술적 의사결정과 팀 업무 조율을 함께 수행해왔다.

## 기술 스택

| 분류 | 기술 |
|------|------|
| Backend | Node.js, TypeScript, NestJS, Prisma ORM |
| Database | MySQL |
| Infrastructure | AWS (EC2, CloudWatch), Docker, Docker Compose, Nginx |
| DevOps | Jenkins, GitLab CI |
| Testing | GTest/GMock, CMake |
| Tools | Git, GitHub, GitLab, Jira, Confluence, Notion, Figma |

## 경력

### Wewake (2024.10 ~ 2025.09)

**차량 S/W 개발 (LG전자 CCU2 프로젝트 파트너)**

LG전자 차량 통신 모듈(MSM) 개발 프로젝트에 참여. C++ 기반 스펙 구현, 단위 테스트 체계 구축, CI/CD 파이프라인 설계, 프로세스 개선을 수행했다.

**기술 스택**: C++, GTest/GMock, CMake, Jenkins, GitLab, Docker, Python

#### 테스트 전략 및 체계 구축

양산된 C++ 제품의 단위 테스트를 형식적 테스트에서 실제 기능 검증 체계로 전환을 도모했다. 규모: 25개 프로덕션 파일, 719개 메서드, 2,073개 테스트 케이스.

- **DI 없는 레거시 코드 테스트**: 코드 수정 불가 제약 하에서 link-time substitution 기반 4단계 Mocking 프로세스 수립. CMake 빌드 설정으로 테스트 시에만 오브젝트 파일 교체
- **테스트 전략**: Manager 클래스의 public API만 직접 테스트, private은 시나리오 기반 간접 검증. 반환값 조작이 필요한 의존성만 Mock (과도한 Mocking 방지)
- **한계와 전환**: 템플릿 추론 및 상속 깊이 문제로 진행 중인 프로젝트에는 전면 적용 실패. 프로젝트 구조를 간소화한 샘플 프로젝트와 GTest/GMock 세미나를 제공하여 다음 프로젝트의 DI 설계 적용 기반 마련

#### CI/CD 파이프라인 설계

- Jenkins + GitLab MR 기반 파이프라인: 커밋 → 빌드 + 단위 테스트 → 바이너리 업로드 → 테스트 리포트 파싱 → Pass/Fail 게이팅 → Slack 알림

#### 정적 분석 및 자동화 도구
반복적이고 비효율적인 작업을 자동화 도구로 대체하여 리드타임 단축 및 품질 관리 프로세스 개선에 기여

- Coverity 정적 분석 운영: 246+ defect 관리, 단계별 리뷰 워크플로우
- Python openpyxl: 설정 DB Excel→JSON 변환 도구
- Linux: 100+ 커밋 로그 자동 파싱, JIRA 티켓 하이퍼링크 생성
  - 고객 요청사항으로 당해 연도 약 100여 개 커밋의 타이틀과 관련 JIRA/CCR 티켓을 정리하는 작업 수행
  - 단순·반복적인 수작업 대신, Git 로그를 스크립트(AWK/grep/sed 등)로 파싱하여 자동화

#### 프로세스 개선

- 문서 중앙화: 개인 PC에 분산된 가이드를 Obsidian+Git(빠른 공유) + Confluence(공식 문서) 2계층 구조로 통합
- 신규 인원 온보딩 가이드 다수 작성 (2년+ 운영 프로젝트의 진입 장벽 해소)
- Jira 이슈 기반 개발 워크플로우 정의, 정적 분석 리뷰 프로세스 수립

---

### OJWare (2023.05 ~ 2024.08)

**BMS 백엔드 개발 리드**

미국 태양광 설치 업체의 태양광 사업 운영 시스템(BMS) 개발. 주문 접수부터 작업 할당, 납품, 청구/결제까지 전체 사업 프로세스를 관리하는 시스템이다. 기획자/개발자가 없는 상황에서 노코드 플랫폼(QuickBase)으로 운영되던 시스템을 분석하고 차세대 시스템을 설계/구현했다. NestJS 기반 백엔드 설계 및 구현, Prisma ORM 데이터 모델링, AWS 인프라 운영을 담당했다. 개발 리드로서 기술적 의사결정과 팀 업무 조율도 수행했다.

**기술 스택**: Node.js, TypeScript, NestJS, Prisma ORM, MySQL, AWS (EC2, CloudWatch), Docker, PM2, Socket.IO, Google Drive API, Gmail API, Mapbox Geocoding API, Census Geocoder API

#### 핵심 기능 구현

**태스크 자동할당 시스템**

하루 평균 200건 주문에서 발생하는 약 1,000개 작업의 수동 할당을 자동화했다.

- Hand Raise(손들기) 시스템: 작업자 요청/취소 API + Socket.IO 실시간 알림
- 3단계 우선순위 알고리즘: Revision 담당자 → 프로젝트 담당자 → 손든 사람(raised_at 순)
- 포지션별 최대 할당 수 제한, 주(State)별 라이센스 기반 할당 필터링 (태양광 설치는 주별 면허 필요)
- 선행 태스크 의존성 기반 Task Flow 활성화 로직

**Job 상태 자동 업데이트 시스템**

Job→Scope→Task 3단계 계층 구조에서 상태 일관성을 자동 유지하는 시스템을 설계/구현했다.

- 7가지 Job 상태 정의 및 전환 규칙 수립 (Not Started, In Progress, On Hold, Completed, Canceled 등)
- 하향식 상태 전파: Job→Scope→Task 자동 전파 + Task→Scope 역전파
- 자동화 최소화 원칙: 경우의 수 과다 영역 식별 → 핵심만 자동화, 나머지는 사용자 선택
- Priority 자동 계산: 작업 시간 경과율 기반 4단계 우선순위, Due Date 변경 시 자동 재계산

**인보이스 시스템**

벤더/클라이언트 인보이스 생성부터 결제, 미수금 관리까지 전 과정을 구현했다.

- 가격 책정: 가정용(기본 가격 + 볼륨 할인) / 상업용(시스템 사이즈 기반 차등 할인, 시간당 과금)
- 조직별 커스텀 가격 + Manual Price 오버라이드 우선순위 로직
- Invoice 생명주기: 월별 자동 생성(이전 달 완료 Job 대상, EST 기준) → Unissued → Issued → Paid
- 분할 지불, Credit(선불금) 시스템, 미수금 집계 쿼리

**AHJ(Authority Having Jurisdiction) 관리**

- 외부 API 연동(Mapbox Geocoding + Census Geocoder)으로 좌표 기반 관할 기관 정보 자동 조회/생성
- DB에 해당 AHJ 없으면 자동 생성, 있으면 재사용

**기타**: Gmail API 수신 연동(스레드 ID 추적, 폴백 로직), User 초대 시스템, Revision 관리(Major/Minor 자동 구분)

#### 인프라 및 운영

**API 서버 안정성 개선**
- 정규 표현식 CPU 과부하 해결: 이미지가 포함될 수 있는 이메일에 정규식 적용 → 싱글스레드 프리징. 정규식 제거로 해결
- 메일을 읽는 서버(IMAP)와 api 서버를 분리하여 서버 프리징 리스크 제거


**CI/CD 및 인프라**
- Docker Compose 멀티 서비스 구성 (API, 스케줄러, Nginx, Certbot)
- SSL/TLS 자동 갱신 (Let's Encrypt)

#### 리더십

- 클라이언트 직접 소통: 요구사항 파악, 기능 범위 확정
- Jira & Confluence 도입, Daily Sync, 1on1 면담, 월간 회고 등 조직 프로세스 체계화

---

### 아워튜브 (2022.02 ~ 2023.05)

**백엔드 총괄**

유튜브 크리에이터의 광고수익금 지분을 거래하는 플랫폼의 백엔드를 총괄했다. 서비스 출시 및 Seed 투자 유치에 기여했다.

**기술 스택**: Node.js, TypeScript, NestJS, MySQL, Docker

#### 핵심 기능 개발

- **입출금 및 거래 시스템**: 입출금 API, 거래 내역 조회, 옥션 입찰 및 분배, 상시거래 기능 구현
- **광고 수익금 분배**: 지분 보유량 스냅샷 기반 수익금 분배 로직 설계 및 구현
- **유튜브 채널 정보 관리**: 채널 데이터 연동 및 관리 기능 개발

#### 데이터 모델링

- 데이터 신뢰성을 위한 이력/내역 테이블 분리 설계
- 여러 프로모션 관리를 위한 M:N 테이블 설계
- general log를 활용한 데이터베이스 특정 시점 복구 경험

#### 인프라

- Docker 도입으로 서버 이전 간편화 — 4회 서버 이전(AWS → NAVER → Azure → Gabia) 수행
- 초기 스타트업의 투자/지원금 조건에 따른 잦은 인프라 변경에 대응

#### 협업

- 기획팀, 디자인팀과 직접 소통하며 기능 구현
- OKR 지표 등 팀에 필요한 데이터 시각화

---

### 로고몬도 (2021.02 ~ 2021.07)

**프론트엔드 개발**

쥬얼리 몰인몰 플랫폼(코너스톤)의 레거시 시스템 유지보수를 담당했다. 처음 접하는 언어와 프레임워크(PHP, Angular)를 학습하여 트러블슈팅을 수행했다.

**기술 스택**: PHP, Angular, JavaScript, HTML/CSS, GCP

- 문서화되지 않은 레거시 코드에서 DevTools 기반 디버깅으로 다수 버그 해결
- GCP 환경 서버 관리
- Grid/Flex 기반 반응형 UI 작업
- 커밋 메시지 작성 문화 주도, 트러블슈팅 과정 문서화 → 이후 팀 전체 Notion 문서화로 확산
