# Kuku

[English](README.md) | 한국어

![GitHub last commit](https://img.shields.io/github/last-commit/kuku-mom/kuku)
![GitHub issues](https://img.shields.io/github/issues/kuku-mom/kuku)
![GitHub stars](https://img.shields.io/github/stars/kuku-mom/kuku)
![License](https://img.shields.io/github/license/kuku-mom/kuku)

집중해서 생각하고 쓰기 위한 로컬 우선 마크다운 데스크톱 앱.

Kuku는 일반 파일 기반 마크다운 편집, 위키링크/백링크, 그래프 뷰, AI 보조 워크플로우(검색/수정/링크)를 Tauri 네이티브 앱 안에서 제공합니다.

현재 **macOS** 지원. Windows/Linux는 로드맵에 있습니다.

![Kuku desktop preview](docs/screenshots/kuku-desktop-preview.png)

## 왜 Kuku인가

Kuku는 "AI를 쓰되 파일 소유권은 내가 가진다"를 목표로 만듭니다.

핵심 제공 기능:
- 내 볼트 기반의 로컬 우선 마크다운 편집
- 위키링크, 백링크, 그래프 탐색
- 변경 승인(diff) 기반의 Cursor 스타일 AI 편집
- 노트 문맥 검색 + 컨텍스트 회수
- Tauri 기반 네이티브 런타임 (Electron 아님)

## 빠른 시작

```bash
pnpm install
pnpm --filter @kuku/desktop tauri:dev
```

데스크톱 번들 빌드:

```bash
pnpm --filter @kuku/desktop tauri build --config apps/desktop/src-tauri/tauri.conf.json
```

워크스페이스 점검:

```bash
pnpm check
pnpm test
```

## 데스크톱 중심 구조

```text
apps/desktop/          # Tauri 데스크톱 앱 (SolidJS + Rust)
apps/server/           # Go API 서버 (인증, AI 엔드포인트)
apps/web/              # 웹사이트/인증/대시보드 (데스크톱 런타임 외곽)
crates/kuku-ai/        # AI 통합 레이어
crates/kuku-indexer/   # 볼트 인덱싱
packages/contract/     # 공유 Connect/proto 계약 (Go + TS)
```

## 앱 핵심 기능

- **Editor**: 슬래시 메뉴/컨텍스트 메뉴/위키링크 삽입이 포함된 마크다운 에디터
- **Graph**: 관계 그래프 시각화 + 백링크 기반 이동
- **AI Chat**: 툴 실행 + 파일 변경 승인 플로우 내장
- **Vault UX**: 빠른 파일 트리, 탭, 키보드 중심 워크플로우

## 플랫폼 노트

- **macOS**: 현재 메인 지원 대상
- **Windows/Linux**: 확장 예정

## 기여

이슈/PR 환영합니다.
큰 변경은 먼저 이슈로 방향을 맞춰주세요.

## 라이선스

[MIT](LICENSE) © kuku-mom
