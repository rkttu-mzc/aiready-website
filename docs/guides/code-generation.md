# 코드 생성 팁

AI를 활용한 효율적인 코드 생성 기법과 실무에서 바로 적용할 수 있는 팁들을 소개합니다.

## 🎯 코드 생성 전략

### 1. 점진적 구현 접근법

큰 기능을 한 번에 요청하지 말고 단계별로 구현해보세요.

#### ❌ 비효율적인 접근

```text
완전한 전자상거래 사이트를 만들어주세요.
```

#### ✅ 효율적인 접근

```text
1단계: 기본 상품 목록 컴포넌트를 만들어주세요.
2단계: 상품 상세 페이지를 추가해주세요.
3단계: 장바구니 기능을 구현해주세요.
4단계: 결제 플로우를 완성해주세요.
```

### 2. 컨텍스트 기반 생성

현재 프로젝트의 컨텍스트를 명확히 제공하세요.

```text
현재 Next.js 13 앱 라우터 프로젝트에서 작업 중입니다.
기존 컴포넌트들은 TypeScript와 TailwindCSS를 사용하고 있고,
상태 관리는 Zustand를 사용합니다.

이 환경에 맞는 사용자 인증 컴포넌트를 만들어주세요.
```

## 🔧 실무 코드 생성 패턴

### React 컴포넌트 생성

#### 기본 패턴

```text
React TypeScript 함수형 컴포넌트를 만들어주세요.

컴포넌트명: UserCard
Props:
- user: { id: string, name: string, email: string, avatar?: string }
- onEdit: (id: string) => void
- onDelete: (id: string) => void

요구사항:
- 반응형 디자인 (모바일 우선)
- 접근성 고려 (ARIA 속성)
- 로딩 상태 처리
- 에러 상태 처리
- TailwindCSS 사용
```

#### 고급 패턴

```text
다음 요구사항에 맞는 React 컴포넌트를 만들어주세요:

1. 컴포넌트 구조:
   - 메인 컴포넌트: DataTable
   - 서브 컴포넌트: TableHeader, TableRow, TableCell

2. 기능:
   - 정렬 (오름차순/내림차순)
   - 필터링 (텍스트 검색)
   - 페이지네이션
   - 행 선택 (단일/다중)

3. 기술 스택:
   - React 18 + TypeScript
   - 상태 관리: useState + useReducer
   - 스타일링: Styled Components
   - 아이콘: React Icons

4. 성능 최적화:
   - React.memo 적용
   - 가상화 (react-window)
   - 디바운싱 (검색)

각 컴포넌트를 별도 파일로 분리하고, 
적절한 타입 정의와 JSDoc 주석을 포함해주세요.
```

### API 엔드포인트 생성

#### Express.js 패턴

```text
Node.js Express를 사용해서 RESTful API를 만들어주세요.

엔드포인트: /api/users
기능: 사용자 CRUD

요구사항:
1. 라우터 구조:
   - GET /api/users - 사용자 목록 (페이지네이션, 검색)
   - GET /api/users/:id - 특정 사용자 조회
   - POST /api/users - 새 사용자 생성
   - PUT /api/users/:id - 사용자 정보 수정
   - DELETE /api/users/:id - 사용자 삭제

2. 미들웨어:
   - 인증 검사 (JWT)
   - 입력 데이터 검증 (Joi)
   - 에러 처리
   - 로깅 (Winston)

3. 데이터베이스:
   - Prisma ORM 사용
   - PostgreSQL 연결
   - 트랜잭션 처리

4. 응답 형식:
   - 성공: { success: true, data: any, message?: string }
   - 실패: { success: false, error: string, code: number }

5. 추가 기능:
   - Rate limiting
   - CORS 설정
   - API 문서화 (Swagger)

TypeScript로 작성하고, 적절한 타입 정의를 포함해주세요.
```

### 데이터베이스 스키마 생성

#### Prisma 스키마 패턴

```text
Prisma를 사용해서 블로그 시스템의 데이터베이스 스키마를 설계해주세요.

엔티티:
1. User (사용자)
   - 기본 정보: id, email, username, password
   - 프로필: firstName, lastName, bio, avatar
   - 메타데이터: createdAt, updatedAt, lastLoginAt

2. Post (게시글)
   - 콘텐츠: title, content, excerpt, slug
   - 상태: published, featured, viewCount
   - 관계: authorId (User와 연결)

3. Category (카테고리)
   - 기본: name, slug, description
   - 계층: parentId (자기 참조)

4. Tag (태그)
   - 기본: name, slug, color

5. Comment (댓글)
   - 콘텐츠: content, status
   - 관계: postId, authorId, parentId

관계 설정:
- User ↔ Post (1:N)
- Post ↔ Category (N:M)
- Post ↔ Tag (N:M)
- Post ↔ Comment (1:N)
- Comment ↔ Comment (대댓글, 1:N)

추가 요구사항:
- 인덱스 최적화
- 제약 조건 설정
- 기본값 정의
- 마이그레이션 고려사항
```

## 🚀 고급 생성 기법

### 1. 테스트 주도 생성

```text
TDD 방식으로 사용자 인증 서비스를 구현해주세요.

1단계: 테스트 케이스 작성
- 유효한 이메일/비밀번호로 로그인 성공
- 잘못된 이메일로 로그인 실패
- 잘못된 비밀번호로 로그인 실패
- JWT 토큰 생성 및 검증
- 비밀번호 해싱 및 검증

2단계: 실패하는 테스트 구현
3단계: 테스트를 통과하는 최소 구현
4단계: 리팩토링

기술 스택: Node.js, Jest, bcrypt, jsonwebtoken
```

### 2. 성능 최적화 중심 생성

```text
고트래픽을 고려한 실시간 채팅 시스템을 구현해주세요.

성능 요구사항:
- 동시 사용자 10,000명 지원
- 메시지 전송 지연 < 100ms
- 메모리 사용량 최적화
- 수평 확장 가능

기술적 고려사항:
1. WebSocket 연결 관리
2. 메시지 큐 (Redis)
3. 로드 밸런싱
4. 데이터베이스 최적화
5. 캐싱 전략

구현 우선순위:
1. 기본 소켓 서버
2. 메시지 브로드캐스팅
3. 룸 관리
4. 사용자 인증
5. 메시지 저장
6. 성능 최적화

각 단계별로 성능 측정 방법도 포함해주세요.
```

### 3. 보안 중심 생성

```text
엔터프라이즈급 보안을 고려한 파일 업로드 API를 구현해주세요.

보안 요구사항:
1. 파일 타입 검증 (MIME 타입, 매직 넘버)
2. 파일 크기 제한
3. 바이러스 스캔 통합
4. 안전한 파일명 생성
5. 접근 권한 제어
6. 업로드 속도 제한
7. 악성 파일 격리

기술 스택:
- Node.js + Express
- Multer (파일 업로드)
- Sharp (이미지 처리)
- AWS S3 (저장소)
- ClamAV (바이러스 스캔)

보안 체크리스트:
- [ ] 파일 업로드 경로 검증
- [ ] 실행 가능한 파일 차단
- [ ] 메타데이터 제거
- [ ] CDN 보안 헤더 설정
- [ ] 로그 및 모니터링

각 보안 조치에 대한 설명과 구현 방법을 포함해주세요.
```

## 🎯 언어별 최적화 팁

### TypeScript

```text
TypeScript 프로젝트에서 다음 기능을 구현해주세요:

기능: 제네릭 기반 API 클라이언트

요구사항:
1. 강력한 타입 안전성
2. 자동완성 지원
3. 런타임 타입 검증
4. 에러 처리 타입화
5. 미들웨어 지원

추가 조건:
- 복잡한 타입도 적절히 추론되어야 함
- 유틸리티 타입 적극 활용
- 조건부 타입으로 유연성 확보
- JSDoc으로 상세한 문서화

예시 사용법도 함께 제공해주세요.
```

### Python

```text
Python FastAPI를 사용해서 AI 모델 서빙 API를 구현해주세요.

요구사항:
1. 비동기 처리로 고성능 확보
2. Pydantic으로 강력한 데이터 검증
3. 자동 API 문서 생성
4. 의존성 주입 패턴
5. 백그라운드 작업 지원

모델 타입:
- 이미지 분류
- 텍스트 감정 분석
- 추천 시스템

성능 최적화:
- GPU 메모리 관리
- 배치 처리
- 모델 캐싱
- 결과 캐싱

Pythonic한 코드 스타일을 유지하면서
타입 힌트를 적극 활용해주세요.
```

## 📝 코드 품질 향상 프롬프트

### 리팩토링 요청

```text
다음 코드를 리팩토링해주세요:

[기존 코드]

개선 목표:
1. 가독성 향상
2. 성능 최적화
3. 유지보수성 증대
4. 테스트 용이성
5. 확장성 고려

적용할 패턴:
- SOLID 원칙
- 디자인 패턴 (적절한 경우)
- 함수형 프로그래밍 (가능한 경우)

변경사항에 대한 자세한 설명과 
Before/After 비교도 포함해주세요.
```

### 코드 리뷰 스타일 검토

```text
코드 리뷰 관점에서 다음 코드를 검토해주세요:

[검토할 코드]

검토 항목:
1. 코딩 스타일 및 컨벤션
2. 성능 및 최적화
3. 보안 취약점
4. 에러 처리
5. 테스트 가능성
6. 문서화 수준

팀 컨벤션:
- [프로젝트별 규칙들]

건설적인 피드백과 구체적인 개선 제안을 
코드 예시와 함께 제공해주세요.
```

## 🚀 다음 단계

효과적인 코드 생성을 마스터했다면:

1. **[디버깅 활용법](debugging-with-ai.md)**: AI를 활용한 문제 해결
2. **[문서화 자동화](documentation.md)**: 코드 문서화 자동화
3. **[프롬프트 라이브러리](../prompt-library/development.md)**: 더 많은 검증된 프롬프트

!!! tip "지속적인 개선"
    AI 도구는 계속 발전하고 있습니다. 새로운 기능과 개선사항을 정기적으로 확인하고 워크플로우를 업데이트하세요.
