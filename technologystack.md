# 기술 스택(※ 본 내용은 기입 예시입니다. 프로젝트에 맞추어 내용을 변경해 주세요)

## 핵심 기술
- TypeScript: ^5.0.0
- Node.js: ^20.0.0
- **AI 모델: claude-3-7-sonnet-20250219 (Anthropic Messages API 2023-06-01) ← 버전 변경 금지**

## 프런트 엔드
- Next.js: ^15.1.3
- React: ^19.0.0
- Tailwind CSS: ^3.4.17
- shadcn/ui: ^2.1.8

## 백엔드
- SQLite: ^3.0.0
- Prisma: ^5.0.0

## 개발 도구
- npm: ^10.0.0
- ESLint: ^9.0.0
- TypeScript: ^5.0.0

---

# API 버전 관리
## 중요한 제한 사항
- API 클라이언트는 `app/lib/api/client.ts`로 중앙 관리
- AI 모델 버전은 client.ts 내에서 엄격하게 관리
- 이러한 파일은 변경 금지(변경이 필요한 경우 승인 필요): 
- client.ts - AI 모델과 API 설정의 핵심 
- types.ts - 형식 정의의 중앙 관리 
- config.ts - 환경 설정의 중앙 관리

## 구현 규칙
- AI 모델 버전은 client.ts에서만 정의
- 형식 정의는 항상 types.ts 참조
- 환경 변수 사용은 config.ts를 통해서만 허용됩니다.