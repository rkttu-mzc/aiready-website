# 효과적인 프롬프팅

프롬프트 엔지니어링은 AI와 효과적으로 소통하는 핵심 기술입니다. 올바른 프롬프트는 원하는 결과를 얻는 것과 실망스러운 결과 사이의 차이를 만듭니다.

## 🎯 프롬프트 엔지니어링 기본 원칙

### 1. 명확성 (Clarity)

#### ❌ 모호한 프롬프트

```text
"웹사이트 만들어줘"
```

#### ✅ 명확한 프롬프트

```text
React와 TypeScript를 사용해서 사용자 인증 기능이 있는 대시보드 웹 애플리케이션을 만들어주세요. 
로그인, 회원가입, 사용자 프로필 페이지가 필요하고, 
TailwindCSS로 모던한 디자인을 적용해주세요.
```

### 2. 구체성 (Specificity)

#### ❌ 일반적인 요청

```text
"코드를 개선해줘"
```

#### ✅ 구체적인 요청

```text
이 React 컴포넌트의 성능을 개선해주세요:
1. 불필요한 리렌더링 방지
2. 메모이제이션 적용
3. 이벤트 핸들러 최적화
4. 변경사항에 대한 설명도 함께 제공해주세요
```

### 3. 컨텍스트 제공 (Context)

#### ✅ 충분한 컨텍스트

```text
현재 Next.js 13 앱 라우터 기반 프로젝트에서 작업하고 있습니다.
기존 인증 시스템은 NextAuth.js를 사용하고 있고,
데이터베이스는 Prisma + PostgreSQL을 사용합니다.

이 환경에서 사용자 권한 관리 미들웨어를 만들어주세요.
관리자, 일반 사용자, 게스트 3단계 권한이 필요합니다.
```

## 📝 프롬프트 템플릿

### 1. 코드 생성 템플릿

```text
[기술 스택] 을 사용해서 [기능 설명] 을 구현해주세요.

요구사항:
- [요구사항 1]
- [요구사항 2]
- [요구사항 3]

제약사항:
- [제약사항 1]
- [제약사항 2]

추가 고려사항:
- [성능/보안/접근성 등]
```

**사용 예시:**

```text
React와 TypeScript를 사용해서 파일 업로드 컴포넌트를 구현해주세요.

요구사항:
- 드래그 앤 드롭 지원
- 다중 파일 선택 가능
- 업로드 진행률 표시
- 파일 크기 및 확장자 제한

제약사항:
- 파일 크기는 10MB 이하
- 이미지 파일만 허용 (jpg, png, gif)

추가 고려사항:
- 접근성을 위한 키보드 네비게이션 지원
- 에러 처리 및 사용자 피드백
```

### 2. 코드 리뷰 템플릿

```text
다음 코드를 리뷰해주세요:

[코드 블록]

검토 항목:
- 코드 품질 및 가독성
- 성능 최적화 가능성
- 보안 취약점
- 베스트 프랙티스 준수
- 테스트 가능성

개선 제안과 함께 수정된 코드를 제공해주세요.
```

### 3. 디버깅 템플릿

```text
다음 오류를 해결해주세요:

오류 메시지:
[오류 메시지]

문제가 발생한 코드:
[코드 블록]

현재 환경:
- [기술 스택 정보]
- [패키지 버전]
- [설정 정보]

시도해본 해결 방법:
- [시도한 방법 1]
- [시도한 방법 2]

해결 방법과 함께 원인 분석도 제공해주세요.
```

## 🎪 고급 프롬프팅 기법

### 1. 역할 설정 (Role Playing)

```text
당신은 시니어 풀스택 개발자입니다. 
10년 이상의 경험을 가지고 있으며, 
특히 React 생태계와 Node.js에 전문성을 가지고 있습니다.

다음 아키텍처 설계 문제를 해결해주세요:
[문제 설명]
```

### 2. 단계별 사고 (Step-by-step Thinking)

```text
대규모 React 애플리케이션의 성능 최적화 계획을 세워주세요.

다음 단계로 접근해주세요:
1. 현재 성능 문제 분석 방법
2. 우선순위 설정 기준
3. 구체적인 최적화 기법들
4. 측정 및 검증 방법
5. 실행 계획 및 타임라인

각 단계마다 구체적인 도구와 방법론을 제시해주세요.
```

### 3. 예시 기반 학습 (Few-shot Learning)

```text
다음과 같은 패턴으로 API 엔드포인트를 만들어주세요:

예시 1:
// GET /api/users
export async function GET() {
  const users = await prisma.user.findMany();
  return NextResponse.json(users);
}

예시 2:
// POST /api/users
export async function POST(request: Request) {
  const body = await request.json();
  const user = await prisma.user.create({ data: body });
  return NextResponse.json(user);
}

이 패턴을 따라서 상품(products) 관리 API를 만들어주세요.
CRUD 모든 기능이 필요하고, 에러 처리도 포함해주세요.
```

### 4. 제약 조건 활용 (Constraint-based)

```text
다음 제약 조건을 모두 만족하는 로그인 폼을 만들어주세요:

기술적 제약:
- Vanilla JavaScript만 사용 (프레임워크 X)
- CSS Grid 또는 Flexbox 사용
- 최대 50줄 이하의 JavaScript 코드

기능적 제약:
- 이메일과 패스워드 검증
- 실시간 에러 메시지 표시
- 로그인 중 버튼 비활성화

디자인 제약:
- 모바일 우선 반응형 디자인
- 최대 2가지 색상만 사용
- 애니메이션 포함
```

## 🔧 실무 활용 시나리오

### 시나리오 1: 레거시 코드 리팩토링

```text
10년 된 jQuery 기반 코드를 모던 JavaScript로 리팩토링해주세요.

원본 코드:
[레거시 코드]

목표:
- ES6+ 문법 사용
- 모듈화 구조
- 테스트 가능한 구조
- 성능 향상

단계별로 마이그레이션 계획도 함께 제공해주세요.
```

### 시나리오 2: 새로운 기술 스택 학습

```text
Vue.js 개발자가 React로 전환하려고 합니다.

Vue 컴포넌트:
[Vue 코드 예시]

이것과 동일한 기능을 React로 구현해주세요.
그리고 Vue와 React의 차이점을 설명하면서 
React 베스트 프랙티스도 함께 알려주세요.
```

### 시나리오 3: 성능 최적화

```text
다음 React 컴포넌트가 성능 문제를 일으키고 있습니다.

[문제가 있는 컴포넌트 코드]

문제점을 분석하고 최적화된 버전을 제공해주세요.
React DevTools Profiler 결과 해석도 포함해주세요.
```

## 📊 프롬프트 품질 평가

### 좋은 프롬프트의 특징

- ✅ 명확한 목표
- ✅ 구체적인 요구사항
- ✅ 충분한 컨텍스트
- ✅ 예상 결과물 명시
- ✅ 제약사항 포함

### 개선이 필요한 신호

- ❌ AI가 질문으로 응답
- ❌ 예상과 다른 결과
- ❌ 너무 일반적인 답변
- ❌ 컨텍스트 무시

## 🎯 프롬프트 최적화 연습

### 연습 1: 프롬프트 개선하기

**Before (개선 전):**

```text
API 만들어줘
```

**After (개선 후):**

```text
Node.js Express를 사용해서 RESTful API를 만들어주세요.

엔드포인트:
- GET /api/tasks - 할일 목록 조회
- POST /api/tasks - 새 할일 생성
- PUT /api/tasks/:id - 할일 수정
- DELETE /api/tasks/:id - 할일 삭제

요구사항:
- MongoDB 연동
- 입력 데이터 검증
- 에러 처리
- API 문서화 (Swagger)

응답 형식은 JSON이고, HTTP 상태 코드를 적절히 사용해주세요.
```

### 연습 2: 컨텍스트 추가하기

문제 상황을 주고 더 나은 프롬프트로 개선해보세요.

## 📚 추가 자료

- **[프롬프트 라이브러리](../prompt-library/development.md)**: 검증된 프롬프트 모음
- **[코드 생성 팁](code-generation.md)**: 실무 코드 생성 기법
- **[디버깅 활용법](debugging-with-ai.md)**: AI를 활용한 문제 해결
