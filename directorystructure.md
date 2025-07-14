# 디렉토리 구성(※ 본 내용은 기입 예시입니다. 프로젝트에 맞추어 내용을 변경해 주세요)

다음 디렉토리 구조에 따라 구현하십시오.

```
/
├── app/                          # Next.js 애플리케이션 디렉토리
│   ├── api/                      # API엔드포인트
│   │   └── [endpoint]/
│   │       └── route.ts
│   ├── components/               # 애플리케이션 컴포넌트
│   │   ├── ui/                   # 기본UI（button, card등）
│   │   └── layout/               # 레이아웃 관련 
│   ├── hooks/                    # 커스텀 훅
│   ├── lib/                      # 유틸리티
│   │   ├── api/                  # API관련 처리 
│   │   │   ├── client.ts         # 변경 금지: AI 모델 설정
│   │   │   ├── types.ts          # 변경 금지: 형식 정의
│   │   │   └── config.ts         # 변경 금지 : 환경 설정
│   │   └── utils/                # 공통 함수
│   ├── styles/                   # 스타일 정의
│   ├── favicon.ico               # 파비콘
│   ├── globals.css               # 글로벌 스타일
│   ├── layout.tsx                # 루트 레이아웃
│   └── page.tsx                  # 홈페이지
├── public/                       # 정적 파일
├── node_modules/                 # 종속 패키지
├── .git/                         # Git 저장소
├── .cursor/                      # Cursor 설정
├── package.json                  # 프로젝트 설정
├── package-lock.json             # 종속성 잠금 파일
├── tsconfig.json                 # TypeScript 설정
├── next-env.d.ts                 # Next.js 타입 정의
├── next.config.ts                # Next.js 설정
├── postcss.config.mjs            # PostCSS 설정
├── eslint.config.mjs             # ESLint 설정
└── .gitignore                    # Git 제외 설정
```

### 배치 규칙
- UI 컴포넌트 → `app/components/ui/`
- API 엔드포인트 → `app/api/[endpoint]/route.ts`
- 공통 처리 → `app/lib/utils/`
- API 관련 처리 → `app/lib/api/`