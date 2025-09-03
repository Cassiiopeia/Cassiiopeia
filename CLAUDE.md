# CLAUDE.md - 프로젝트 가이드라인

## 🚨 중요 규칙

### 1. **자동 커밋 금지**
- 절대 커밋 여부를 묻지 않음
- 자동 커밋 금지
- 사용자가 알아서 커밋함

### 2. **GitHub 정보**
- GitHub 사용자명: `Cassiiopeia`
- 프로젝트 저장소: `https://github.com/Cassiiopeia/Cassiiopeia`
- Personal Access Token: `_GITHUB_PAT_TOKEN` 

## 📝 개발 명령어

### **매우 중요한 CLI 명령어 사용법**
모든 명령어 실행 시 다음 형식을 사용해야 정상 작동합니다:

```bash
source ~/.zshrc && [실행할 명령어]
```

#### 예시:
```bash
# 빌드 실행
source ~/.zshrc && npm run build

# 테스트 실행
source ~/.zshrc && npm test

# 린트 체크
source ~/.zshrc && npm run lint

# 타입 체크
source ~/.zshrc && npm run typecheck
```

## 🔧 프로젝트 특이사항

### WakaTime 설정
- GitHub Actions에서 `_GITHUB_PAT_TOKEN` 사용 (GITHUB_TOKEN이 아님)
- WakaTime API Key는 `WAKATIME_API_KEY` Secret으로 저장

### 작업 플로우
1. 이슈 확인 및 분석
2. 코드 수정
3. 테스트 실행 (source ~/.zshrc && 명령어)
4. 사용자에게 변경사항 보고
5. 사용자가 요청 시에만 커밋 수행

## 📌 주의사항
- 모든 bash 명령어는 `source ~/.zshrc &&` 프리픽스 필수
- 커밋은 사용자 요청 시에만 수행
- GitHub PAT는 `_GITHUB_PAT_TOKEN` 사용 