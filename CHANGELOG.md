# Changelog

**현재 버전:** 1.2.2  
**마지막 업데이트:** 2026-01-01T11:53:41Z  

---

## [1.2.2] - 2026-01-01

**PR:** #9  

NoteModernizes project automation and documentation.

CI/Workflows: Replaces/updates changelog pipeline to parse PR body Markdown, auto-sets deploy titles, robust summary polling/merging; improves README version updater with strict validation and clearer errors; adds QA issue creation bot (default assignee support); replaces API-based issue helper with module-based workflow; disables old API workflow; removes several legacy workflows
Scripts: Refactors changelog_manager.py to Markdown parsers with fallback strategies and cleaner output; upgrades version_manager.sh to v3.0 using yq/jq, required-tool checks, safer per-project updates; adds .cursor/scripts/common_util.py and docs for Windows-safe file ops
Docs/Templates: Adds/aligns analyze, design-analyze, design, implement, plan, ppt, refactor-analyze, report, test, testcase command guides under .claude/ and .cursor/, clarifying workflows and checklists
Config: Tweaks .coderabbit.yaml (disable poem, issue enrichment), updates .gitignore to ignore /.report

Written by Cursor Bugbot for commit 86a51f1. This will update automatically on new commits. Configure here.

Summary by CodeRabbit
릴리스 노트

새로운 기능

포괄적인 개발 워크플로우 가이드 문서 추가 (계획, 분석, 구현, 검토, 테스트)
SUH-DEVOPS-TEMPLATE 설정 가이드 추가
테스트 케이스 생성 및 구현 보고서 자동화 도구 추가

개선사항

버전 1.1.2에서 1.2.2로 업그레이드
README 디자인 및 프로젝트 정보 개선
GitHub 액션 워크플로우 최적화
공통 유틸리티 스크립트 추가로 개발 생산성 향상

---

## [1.1.2] - 2025-11-25

**PR:** #4  

**새로운 기능**
- GitHub Actions 자동화를 통한 PR 및 이슈 처리 개선
- QA 요청 자동 생성 및 추적 기능 추가
- 자동 변경사항 로그 생성 및 배포 파이프라인 구축

**문서화**
- 다중 프레임워크(Spring Boot, React, Flutter) 개발 가이드 추가
- 분석, 구현, 테스트, 리팩토링 모드별 워크플로우 문서화
- 개발자 협업 규칙 및 코드 스타일 가이드 정의

**개선사항**
- 버전 관리 시스템 개선 (1.0.2 → 1.1.2)
- Windows 환경 파일 작업 유틸리티 추가
- 자동 버전 제어 워크플로우 구현

---

