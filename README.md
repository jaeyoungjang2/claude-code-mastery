## Learn More

공식 문서는 아래에서 확인할 수 있습니다.

[Official Documentation](https://code.claude.com/docs/en/overview)

<img src="./demo.gif" />

---

# Claude Code 사용 가이드

## 진행 과정

Claude Code를 사용할 때의 기본 흐름은 다음과 같습니다.

1. **탐색**
   - 필요한 정보를 수집합니다.

2. **계획 수립**
   - `think mode`를 사용합니다.
   - 확장된 사고를 통해 계획을 수립합니다.

3. **구현**
   - 구현과 검증을 동시에 요청합니다.

4. **커밋**
   - 작업 완료 후 Git에 push 합니다.

---

> [!NOTE]
> Installation via npm is deprecated. Use one of the recommended methods below.

추가 설치 옵션, 제거 방법, 트러블슈팅은 아래 문서를 참고하세요.

[Setup Documentation](https://code.claude.com/docs/en/setup)

---

# 시작하기

## 1. Claude Code 설치

### MacOS / Linux (권장)

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

## 2. 프로젝트 초기화

```bash
/init
```

`/init` 명령을 실행하면 Claude Code가 프로젝트를 분석하여 다음 내용을 확인합니다.

- 프로젝트 구조
- 기술 스택
- 코드 컨벤션

그리고 `CLAUDE.md` 파일을 생성합니다.

프로젝트 규모가 큰 경우에는 아래 명령어를 사용할 수 있습니다.

```bash
/init ultrathink
```

---

# 주요 명령어

## 기본 명령어

| 명령어 | 설명 |
|---|---|
| `Ctrl + T` | 진행 상황 확인 (Todo List 확인 가능) |
| `/context` | 현재 사용 중인 context 양 확인 |
| `/clear` | 토큰 초기화 |
| `/init` | 프로젝트 구조, 기술 스택, 컨벤션 분석 후 `CLAUDE.md` 생성 |
| `/init ultrathink` | 대규모 프로젝트 분석 시 사용 |
| `/memory` | 메모리 관련 기능 |
| `/help` | 도움말 확인 |
| `/status` | 현재 상태 확인 |
| `/doctor` | 상태 진단 |
| `/usage` | 사용량 조회 |
| `/resume` | 이전 세션 목록 확인 |
| `/rename <현재 세션 이름>` | 현재 세션 이름 변경 |
| `/model` | 모델 변경 |
| `/compact` | 대화 내용을 요약하여 context 정리 |
| `/statusline` | 하단 상태 바 생성 |
| `/output-style` | 출력 스타일 설정 |
| `/bashes` | 백그라운드 작업 확인 가능 |

---

# Statusline

`/statusline` 명령을 사용하면 하단 상태 바를 생성할 수 있습니다.

표시 예시:
- 모델명
- 컨텍스트 라인
- 비용

---

# Output Style

출력 스타일을 지정하여 응답 방식을 조정할 수 있습니다.

## 예시 스타일

- **Explanatory**
   - 설명을 함께 추가하는 스타일

- **Learning**
   - 학습용 스타일

스타일 파일은 아래 경로에 작성하면 됩니다.

```bash
output-styles/beginner.md
```

추가 조작:

- `Shift + Tab`
   - 모드 변경

- `Esc`
   - 작업 준비 또는 작업 흐름 전환 시 사용

---

# 프로젝트 세팅 예시

## Next.js 설치

Next.js 프로젝트를 설치합니다.

## shadcn/ui 설치

UI 컴포넌트 구성을 위해 `shadcn/ui`를 설치합니다.

---

# 문제 해결 방식

## plan

문제를 단계별로 생각해서 해결할 수 있도록 계획을 세웁니다.  
이때 **CoT(Chain of Thought) 프롬프트**를 활용합니다.

## split

단계별 해결 계획을 실제 실행 가능한 작업 단위로 나누어 수행합니다.

---

# Playwright

## Playwright란?

Playwright는 웹 브라우저 자동화 도구입니다.

다음과 같은 작업에 활용할 수 있습니다.

- 모든 주요 브라우저 제어
- 자동 테스트 수행
- 화면 캡처
- 브라우저 기반 작업 자동화

## Playwright MCP 설치

```bash
claude mcp add playwright npx @playwright/mcp@latest --scope project
```

---

# 오류 해결 프로세스

오류가 발생했을 때는 아래 순서로 진행합니다.

1. 오류 정보 수집
2. 오류 원인 분석
3. 오류 해결
4. 테스트

오류가 해결되지 않으면 다시 1번부터 반복합니다.  
즉, **오류가 해결될 때까지 반복적으로 점검합니다.**

## 오류 정보 제공 예시

- 오류 1
- 오류 2