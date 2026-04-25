# GitHub Profile README 전면 개편 스펙

## 목표

현재 README의 가독성 저하, About Me 섹션 어색함, MY LAB 존재감 부족, Featured Projects outdated 문제를 해결한다. 전체 레이아웃을 심플하고 읽기 쉬운 구조로 개편한다.

---

## 섹션 구성 (위→아래 순서)

### 1. Hero 헤더 — 개편

현재 capsule-render 배너 + typing-svg 유지. 변경 없음.

### 2. MY LAB — 신설

- 상단 뱃지에서 **별도 섹션**으로 분리, Hero 바로 아래 배치
- 배경: GitHub 다크 (`#161b22`, border `#30363d`)
- 텍스트: `lab.suhsaechan.kr` (URL 강조색 `#79c0ff`) + 한 줄 설명
- 설명: `제가 만든 모든 것이 여기에 있어요.`
- 링크: `https://lab.suhsaechan.kr`

### 3. About Me — 제거

기존 테이블형 About Me 섹션 삭제. Spec 섹션으로 대체.

### 4. Spec — 신설

뱃지 없이 텍스트 테이블로만 구성.

| 항목 | 내용 |
|------|------|
| Work | Somansa DLP · Software Programmer · Jul 2024 – Present |
| Edu | Sejong Univ. · Bio-convergence Engineering · GPA 3.8 · 2018–2024 |
| Cert | Engineer Information Processing · SQLD · Linux Master Lv.2 · Chemical Analysis Engineer |
| Location | Seoul, South Korea |
| Open to | Collaboration & Side Projects |

### 5. Projects — 전면 교체

기존 Featured Projects(Malsami 포함) 제거. 불릿 리스트형으로 교체.

| 프로젝트 | 설명 | 링크 |
|----------|------|------|
| RomRom | AI-powered barter platform — match items, get AI pricing, trade smarter | Google Play · App Store · BE · FE |
| SUH-DEVOPS-TEMPLATE | Full dev cycle automation — issue to deploy, powered by GitHub Actions & AI | Repo |
| Tripgether | AI travel guide — extracts places from SNS posts, builds your personal map | BE · FE |
| PassQL | Password management library & web service | passql.vercel.app · Repo |
| Re: WAVE | Choice-driven visual novel — your decisions shape the story | bagel.suhsaechan.kr · Repo |
| suh-project-utility | Personal dev lab — experiments, utilities, and tools I actually use | lab.suhsaechan.kr · Repo |

링크 URL:
- RomRom Google Play: `https://play.google.com/store/apps/details?id=com.alom.romrom`
- RomRom App Store: `https://apps.apple.com/kr/app/id6748823976`
- RomRom BE: `https://github.com/TEAM-ROMROM/RomRom-BE`
- RomRom FE: `https://github.com/TEAM-ROMROM/RomRom-FE`
- SUH-DEVOPS-TEMPLATE: `https://github.com/Cassiiopeia/SUH-DEVOPS-TEMPLATE`
- Tripgether BE: `https://github.com/Cassiiopeia/Tripgether-BE`
- Tripgether FE: `https://github.com/Cassiiopeia/tripgether-FE`
- PassQL: `https://passql.vercel.app/` · `https://github.com/passQL-Lab/passQL`
- Re: WAVE: `https://bagel.suhsaechan.kr/` · `https://github.com/bagle-ggul/Bagel-Backend`
- suh-project-utility: `https://lab.suhsaechan.kr` · `https://github.com/Cassiiopeia/suh-project-utility`

### 6. Open Source Modules — 신설

모듈명 · 설명 · Repo 링크 목록형.

| 모듈 | 설명 | 링크 |
|------|------|------|
| SUH-Logger | AOP-based JSON logger · auto execution time tracking | `https://github.com/Cassiiopeia/suh-logger` |
| SUH-API-Log | API changelog via JSON · auto Swagger display | `https://github.com/Cassiiopeia/suh-api-log` |
| SUH-Random-Engine | 960K-combo nickname generator · gacha system | `https://github.com/Cassiiopeia/suh-random-engine` |
| SUH-AIder | AI helper library for Spring Boot · OpenAI / Claude | `https://github.com/Cassiiopeia/SUH-AIder` |

### 7. Tech Stack — 유지

현재 테이블 그대로. 내용 변경 없음.

### 8. GitHub Stats — 유지

3D Contribution, Snake Animation, WakaTime 자동 동기화 섹션 그대로.

### 9. 최신 버전 섹션 — footer로 이동

현재 About Me 위에 있는 버전 표시를 README 맨 아래로 이동.

---

## 제거 항목

- About Me 테이블 섹션
- Featured Projects 기존 카드 그리드 (Malsami, 기존 RomRom 카드 등)
- Hero 아래 MY-LAB 뱃지 (별도 섹션으로 이동했으므로)

---

## 파일

- 수정 대상: `README.md` (단일 파일)
- 자동 동기화 섹션(`<!-- 수정하지마세요 -->` 주석 포함 블록)은 건드리지 않음
