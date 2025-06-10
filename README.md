# CTU Gen AI 활용 가이드

CTU(Cloud Tech Unit)의 생성형 AI 효과적 활용을 위한 종합 문서화 사이트입니다.

## 🚀 바로 시작하기

### 로컬 개발 환경 설정

1. **저장소 클론**
```bash
git clone https://github.com/aiready-website/aiready-website.git
cd aiready-website
```

2. **Python 가상환경 생성 및 활성화**
```bash
python -m venv mkdocs-env
mkdocs-env\Scripts\activate  # Windows
# source mkdocs-env/bin/activate  # macOS/Linux
```

3. **의존성 설치**
```bash
pip install -r requirements.txt
```

4. **개발 서버 실행**
```bash
mkdocs serve
```

사이트는 `http://127.0.0.1:8000`에서 확인할 수 있습니다.

## 📁 프로젝트 구조

```
aiready-website/
├── docs/                          # 문서 소스 파일들
│   ├── index.md                   # 홈페이지
│   ├── getting-started/           # 시작하기 가이드
│   ├── guides/                    # AI 활용 가이드
│   ├── prompt-library/            # 프롬프트 라이브러리
│   ├── cursor-rules/              # Cursor 규칙 모음
│   ├── api/                       # API 참조
│   ├── stylesheets/               # 커스텀 CSS
│   └── javascripts/               # 커스텀 JavaScript
├── .github/workflows/             # GitHub Actions
├── mkdocs.yml                     # MkDocs 설정
├── requirements.txt               # Python 의존성
└── README.md                      # 이 파일
```

## 🌟 주요 기능

- **종합 AI 가이드**: 효과적인 프롬프팅부터 고급 활용법까지
- **프롬프트 라이브러리**: 즉시 사용 가능한 검증된 프롬프트 모음
- **Cursor 규칙 파일**: 프로젝트별 맞춤 AI 어시스턴트 설정
- **실무 중심**: CTU의 실제 경험을 바탕으로 한 실용적 내용
- **지속적 업데이트**: 최신 AI 도구와 기법 반영

## 🛠️ 기술 스택

- **문서화**: MkDocs + Material for MkDocs
- **호스팅**: GitHub Pages
- **자동 배포**: GitHub Actions
- **스타일링**: TailwindCSS + 커스텀 CSS
- **기능 향상**: Python 확장 및 플러그인

## 🤝 기여하기

1. **이슈 생성**: 개선사항이나 버그 리포트
2. **Fork & Pull Request**: 직접 문서 수정 및 기여
3. **피드백 제공**: 사용 경험 공유

### 문서 작성 가이드

새 문서를 추가하거나 기존 문서를 수정할 때:

1. `docs/` 디렉터리에서 마크다운 파일 편집
2. `mkdocs.yml`의 `nav` 섹션에 새 페이지 추가
3. 로컬에서 `mkdocs serve`로 테스트
4. 변경사항 커밋 및 푸시

## 📈 배포

### 자동 배포
- `main` 브랜치에 푸시하면 GitHub Actions가 자동으로 배포
- 배포 상태는 Actions 탭에서 확인 가능

### 수동 배포
```bash
mkdocs gh-deploy
```

## 🔗 관련 링크

- **라이브 사이트**: [https://aiready-website.github.io/aiready-website/](https://aiready-website.github.io/aiready-website/)
- **MkDocs 문서**: [https://www.mkdocs.org/](https://www.mkdocs.org/)
- **Material for MkDocs**: [https://squidfunk.github.io/mkdocs-material/](https://squidfunk.github.io/mkdocs-material/)

## 📞 문의

- **이슈 트래커**: [GitHub Issues](https://github.com/aiready-website/aiready-website/issues)
- **이메일**: tech@ctu.dev
- **Discord**: [CTU 개발자 커뮤니티](https://discord.gg/ctu-tech)

---

**CTU Gen AI 활용 가이드**와 함께 더 효율적이고 스마트한 개발을 경험해보세요! 🚀
AIR Boost / AI Ready Web Site
