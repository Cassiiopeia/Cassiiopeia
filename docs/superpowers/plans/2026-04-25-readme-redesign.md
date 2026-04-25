# README Redesign Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** GitHub 프로필 README를 전면 개편 — MY LAB 섹션 신설, About Me 제거, Spec/Projects/Open Source Modules 섹션 교체

**Architecture:** 단일 파일 `README.md` 수정. 자동 동기화 주석 블록(`<!--START_SECTION:waka-->` ~ `<!--END_SECTION:waka-->`, `<!-- 수정하지마세요 -->` 블록)은 절대 건드리지 않는다. 섹션을 위에서 아래로 순서대로 교체한다.

**Tech Stack:** Markdown, GitHub-flavored HTML (img, p, table 태그), shields.io 뱃지

---

## 파일 구조

- **수정**: `README.md` (단일 파일, 전체 재작성)

---

### Task 1: Hero + MY LAB 섹션 교체

현재 Hero 아래 MY-LAB 뱃지 제거, MY LAB 전용 섹션 신설. About Me 섹션 완전 제거.

**Files:**
- Modify: `README.md:1-51`

- [ ] **Step 1: README 상단 — Hero는 유지, MY LAB 뱃지 제거 후 섹션 신설**

`README.md` 파일 상단(1~51번째 줄)을 아래 내용으로 교체한다.

```markdown
<!-- Cassiiopeia's GitHub Profile README -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:7F7FD5,100:86A8E7&height=180&section=header&text=Suh%20Saechan&fontSize=50&fontColor=FFFFFF&fontAlign=50&fontAlignY=35&animation=fadeIn" alt="header"/>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=2500&pause=1000&color=6A5ACD&center=true&vCenter=true&width=500&lines=Backend+Engineer+%40+Somansa;Building+Scalable+Systems+with+Java+%26+Spring;AI+%2B+Side+Projects+Enthusiast;Always+Open+to+Collaborate" alt="typing"/>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=Cassiiopeia&style=flat-square&color=7F7FD5" alt="profile views"/>
  <img src="https://img.shields.io/badge/Somansa-Server_Module_Team-1f425f?style=flat-square" alt="Somansa"/>
</p>

<a href="https://lab.suhsaechan.kr">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=161b22&height=80&text=lab.suhsaechan.kr&fontColor=79c0ff&fontSize=28&fontAlign=50&fontAlignY=45&desc=%EC%A0%9C%EA%B0%80%20%EB%A7%8C%EB%93%A0%20%EB%AA%A8%EB%93%A0%20%EA%B2%83%EC%9D%B4%20%EC%97%AC%EA%B8%B0%EC%97%90%20%EC%9E%88%EC%96%B4%EC%9A%94.&descFontColor=8b949e&descFontSize=14&descAlign=50&descAlignY=75&borderRadius=6" width="100%" alt="MY LAB"/>
</a>

---
```

- [ ] **Step 2: 변경 내용 확인**

`README.md` 1~35번째 줄을 읽어 Hero 배너, typing-svg, komarev, Somansa 뱃지, MY LAB 섹션이 순서대로 있고 기존 About Me 테이블이 없는지 확인한다.

---

### Task 2: Spec 섹션 삽입

기존 버전 표시 블록 앞에 Spec 섹션을 삽입한다.

**Files:**
- Modify: `README.md` — `---` 구분선 직후, `<!-- 수정하지마세요 -->` 블록 앞

- [ ] **Step 1: Spec 섹션 삽입**

기존 `---` 다음 줄부터 `<!-- 수정하지마세요 자동으로 동기화 됩니다 -->` 바로 앞에 아래 내용을 삽입한다.

```markdown
## Spec

| | |
|:--|:--|
| 🏢 Work | Somansa DLP · Software Programmer · Jul 2024 – Present |
| 🎓 Edu | Sejong Univ. · Bio-convergence Engineering · GPA 3.8 · 2018–2024 |
| 📜 Cert | Engineer Information Processing · SQLD · Linux Master Lv.2 · Chemical Analysis Engineer |
| 📍 Location | Seoul, South Korea |
| 🤝 Open to | Collaboration & Side Projects |

---

```

- [ ] **Step 2: 확인**

삽입된 Spec 섹션이 자동 동기화 주석 블록(`<!-- 수정하지마세요 -->`) 앞에 위치하는지 확인한다.

---

### Task 3: Featured Projects 섹션 교체

기존 카드 그리드(`## 🚀 Featured Projects` ~ `</table>`) 전체를 제거하고 Projects + Open Source Modules 섹션으로 교체한다.

**Files:**
- Modify: `README.md` — `## 🚀 Featured Projects` 블록 전체

- [ ] **Step 1: Featured Projects 제거 후 새 섹션 삽입**

`## 🚀 Featured Projects` 부터 닫는 `</table>` 태그까지 전체를 아래 내용으로 교체한다.

```markdown
## Projects

| Project | | Links |
|:--------|:--|------:|
| **RomRom** | AI-powered barter platform — match items, get AI pricing, trade smarter | [![Google Play](https://img.shields.io/badge/Google_Play-414141?style=flat-square&logo=google-play&logoColor=white)](https://play.google.com/store/apps/details?id=com.alom.romrom) [![App Store](https://img.shields.io/badge/App_Store-000000?style=flat-square&logo=apple&logoColor=white)](https://apps.apple.com/kr/app/id6748823976) [![BE](https://img.shields.io/badge/BE-6DB33F?style=flat-square&logo=spring&logoColor=white)](https://github.com/TEAM-ROMROM/RomRom-BE) [![FE](https://img.shields.io/badge/FE-02569B?style=flat-square&logo=flutter&logoColor=white)](https://github.com/TEAM-ROMROM/RomRom-FE) |
| **SUH-DEVOPS-TEMPLATE** | Full dev cycle automation — issue to deploy, powered by GitHub Actions & AI | [![Repo](https://img.shields.io/badge/Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Cassiiopeia/SUH-DEVOPS-TEMPLATE) |
| **Tripgether** | AI travel guide — extracts places from SNS posts, builds your personal map | [![BE](https://img.shields.io/badge/BE-6DB33F?style=flat-square&logo=spring&logoColor=white)](https://github.com/Cassiiopeia/Tripgether-BE) [![FE](https://img.shields.io/badge/FE-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Cassiiopeia/tripgether-FE) |
| **PassQL** | Password management library & web service | [![Web](https://img.shields.io/badge/passql.vercel.app-000000?style=flat-square&logo=vercel&logoColor=white)](https://passql.vercel.app/) [![Repo](https://img.shields.io/badge/Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/passQL-Lab/passQL) |
| **Re: WAVE** | Choice-driven visual novel — your decisions shape the story | [![Web](https://img.shields.io/badge/bagel.suhsaechan.kr-161b22?style=flat-square&logo=googlechrome&logoColor=white)](https://bagel.suhsaechan.kr/) [![Repo](https://img.shields.io/badge/Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/bagle-ggul/Bagel-Backend) |
| **suh-project-utility** | Personal dev lab — experiments, utilities, and tools I actually use | [![Web](https://img.shields.io/badge/lab.suhsaechan.kr-161b22?style=flat-square&logo=googlechrome&logoColor=white)](https://lab.suhsaechan.kr) [![Repo](https://img.shields.io/badge/Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Cassiiopeia/suh-project-utility) |

---

## Open Source Modules

| Module | | |
|:-------|:--|--:|
| **SUH-Logger** | AOP-based JSON logger · auto execution time tracking | [![Repo](https://img.shields.io/badge/Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Cassiiopeia/suh-logger) |
| **SUH-API-Log** | API changelog via JSON · auto Swagger display | [![Repo](https://img.shields.io/badge/Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Cassiiopeia/suh-api-log) |
| **SUH-Random-Engine** | 960K-combo nickname generator · gacha system | [![Repo](https://img.shields.io/badge/Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Cassiiopeia/suh-random-engine) |
| **SUH-AIder** | AI helper library for Spring Boot · OpenAI / Claude | [![Repo](https://img.shields.io/badge/Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Cassiiopeia/SUH-AIder) |

---
```

- [ ] **Step 2: 확인**

`## 🚀 Featured Projects`, Malsami 관련 내용, 기존 `<table>` 블록이 완전히 제거됐는지 확인한다. Projects / Open Source Modules 두 섹션이 올바르게 들어갔는지 확인한다.

---

### Task 4: 최신 버전 섹션 footer로 이동

현재 About Me 위에 있던 버전 표시가 이미 제거됐으므로, README 맨 아래 footer capsule-render 바로 앞으로 이동한다.

**Files:**
- Modify: `README.md` — 맨 마지막 footer 직전

- [ ] **Step 1: 버전 섹션 위치 확인**

`<!-- 수정하지마세요 자동으로 동기화 됩니다 -->` 블록이 Task 1에서 이미 제거됐는지 확인. 제거됐다면 footer(`capsule-render` footer img) 바로 앞에 아래를 삽입한다.

```markdown
<!-- 수정하지마세요 자동으로 동기화 됩니다 -->
## 최신 버전 : v1.2.2 (2026-01-01)
[전체 버전 기록 보기](CHANGELOG.md)

---

```

- [ ] **Step 2: 최종 README 전체 구조 확인**

README를 처음부터 끝까지 읽어 아래 순서가 맞는지 확인한다.

1. Hero (capsule-render + typing-svg + komarev/Somansa 뱃지)
2. MY LAB (capsule-render rect 다크 배경)
3. `---`
4. Spec 테이블
5. `---`
6. 버전 섹션 (`<!-- 수정하지마세요 -->`)
7. `---`
8. Projects 테이블
9. `---`
10. Open Source Modules 테이블
11. `---`
12. Tech Stack (기존 그대로)
13. `---`
14. GitHub Stats (기존 그대로)
15. `---`
16. Coding Stats / WakaTime (`<!--START_SECTION:waka-->` ~ `<!--END_SECTION:waka-->`)
17. `---`
18. Footer (capsule-render)
