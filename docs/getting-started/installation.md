# 설치 및 설정

## 필수 도구 설치

### 1. Cursor IDE

!!! info "Cursor란?"
    Cursor는 AI가 내장된 차세대 코드 에디터로, GPT-4를 기반으로 한 코드 생성 및 편집 기능을 제공합니다.

#### 설치 방법

1. [Cursor 공식 웹사이트](https://cursor.sh/) 방문
2. 운영체제에 맞는 버전 다운로드
3. 설치 프로그램 실행

#### 기본 설정

```json
{
  "cursor.ai.model": "gpt-4",
  "cursor.ai.enableCompletion": true,
  "cursor.ai.enableChat": true,
  "cursor.ai.contextLength": 8000
}
```

### 2. GitHub Copilot

#### 설치 (VS Code 사용 시)

1. VS Code Extensions에서 "GitHub Copilot" 검색
2. Install 클릭
3. GitHub 계정으로 인증

#### 설정 확인

```json
{
  "github.copilot.enable": {
    "*": true,
    "yaml": true,
    "plaintext": false,
    "markdown": true
  }
}
```

### 3. 터미널 AI 도구

#### Shell GPT 설치

```bash
# npm을 통한 설치
npm install -g shell-gpt

# 또는 pip을 통한 설치
pip install shell-gpt
```

#### 설정

```bash
# API 키 설정
sgpt --install
```

## 브라우저 확장 프로그램

### 1. ChatGPT 확장 프로그램

- **Chrome**: ChatGPT for Google
- **Edge**: Bing Chat
- **Firefox**: ChatGPT Sidebar

### 2. 코드 분석 도구

- **Codeium**: 무료 AI 코드 완성
- **Tabnine**: 컨텍스트 기반 코드 제안

## 개발 환경 최적화

### 1. .gitignore 설정

```gitignore
# AI 도구 관련
.cursor/
.copilot/
.ai-cache/

# 환경 설정
.env.local
.env.ai
api_keys.txt
```

### 2. 환경 변수 설정

```bash
# Windows PowerShell
$env:OPENAI_API_KEY = "your-api-key-here"
$env:ANTHROPIC_API_KEY = "your-anthropic-key"

# Linux/Mac
export OPENAI_API_KEY="your-api-key-here"
export ANTHROPIC_API_KEY="your-anthropic-key"
```

### 3. 프로젝트별 설정 파일

#### .cursorules 파일 생성

```text
You are an expert developer focused on:
- Clean, maintainable code
- Following project conventions
- Security best practices
- Performance optimization

When suggesting code:
1. Follow the existing code style
2. Add appropriate comments
3. Consider error handling
4. Suggest tests when relevant
```

## API 키 관리

### 1. 보안 가이드라인

- API 키는 절대 코드에 하드코딩하지 않기
- 환경 변수 또는 보안 저장소 사용
- 정기적인 키 로테이션

### 2. 키 저장 방법

#### Windows

```powershell
# Windows Credential Manager 사용
cmdkey /add:openai /user:api /pass:your-api-key
```

#### macOS

```bash
# Keychain 사용
security add-generic-password -a $USER -s openai-api -w your-api-key
```

#### Linux

```bash
# GPG를 이용한 암호화 저장
echo "your-api-key" | gpg --armor --encrypt -r your-email@example.com > api_key.gpg
```

## 설정 검증

### 1. Cursor 동작 확인

```javascript
// 이 주석 다음에 Cursor가 자동완성을 제안하는지 확인
// TODO: 간단한 함수를 만들어보세요
function
```

### 2. GitHub Copilot 테스트

```python
# 이 주석 후에 Copilot이 코드를 제안하는지 확인
# 피보나치 수열을 생성하는 함수
def fibonacci
```

### 3. API 연결 테스트

```bash
# Shell GPT 테스트
sgpt "hello world를 출력하는 Python 코드"

# curl을 이용한 직접 테스트
curl -H "Authorization: Bearer $OPENAI_API_KEY" \
     -H "Content-Type: application/json" \
     -d '{"model":"gpt-3.5-turbo","messages":[{"role":"user","content":"Hello"}]}' \
     https://api.openai.com/v1/chat/completions
```

## 문제 해결

### 자주 발생하는 문제

#### 1. API 키 인식 안됨

```bash
# 환경 변수 확인
echo $OPENAI_API_KEY

# 재설정
source ~/.bashrc  # Linux/Mac
# 또는 PowerShell 재시작 (Windows)
```

#### 2. Cursor AI 기능 비활성화

1. `Ctrl+Shift+P` → "Cursor: Enable AI"
2. 설정에서 AI 기능 확인
3. 계정 로그인 상태 확인

#### 3. 네트워크 연결 문제

```bash
# 프록시 설정 확인
echo $HTTP_PROXY
echo $HTTPS_PROXY

# 방화벽 설정 확인 (기업 네트워크)
```

## 다음 단계

설치가 완료되었다면:

1. **[첫 걸음](quick-start.md)**에서 기본 사용법을 익혀보세요
2. **[효과적인 프롬프팅](../guides/effective-prompting.md)**으로 AI와의 소통법을 배워보세요
3. **[프롬프트 라이브러리](../prompt-library/development.md)**에서 유용한 프롬프트를 찾아보세요
