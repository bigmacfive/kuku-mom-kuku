# Kuku

[English](README.md) | 한국어

집중해서 생각하고 쓰기 위한 로컬 우선 마크다운 데스크톱 앱.

- **Desktop** — macOS용 Tauri + SolidJS 앱
- **AI** — 앱 내부 검색/수정/링크 워크플로우 (변경 승인 기반)
- **Data** — 사용자 볼트의 일반 마크다운 파일

## Screens

<table>
  <tr>
    <th>Workspace Shell</th>
    <th>Provider Setup</th>
  </tr>
  <tr>
    <td><img src="docs/screenshots/kuku-screen-1.png" alt="Kuku workspace shell" /></td>
    <td><img src="docs/screenshots/kuku-screen-2-settings.png" alt="Kuku provider setup" /></td>
  </tr>
  <tr>
    <td>볼트 트리, 에디터, 유틸리티 레일이 포함된 데스크톱 작업 화면.</td>
    <td>프로바이더/키 설정과 데스크톱 AI 설정 화면.</td>
  </tr>
  <tr>
    <th>Search Surface</th>
    <th>Search With Query</th>
  </tr>
  <tr>
    <td><img src="docs/screenshots/kuku-screen-3-search.png" alt="Kuku search surface" /></td>
    <td><img src="docs/screenshots/kuku-screen-4-search-query.png" alt="Kuku search with query" /></td>
  </tr>
  <tr>
    <td>앱 내부 전체 볼트 검색을 위한 고급 검색 화면.</td>
    <td>쿼리 입력 후 빠른 탐색/이동 상태 화면.</td>
  </tr>
</table>

## 왜 Kuku인가

- 내 파일 기반 로컬 우선 마크다운 편집
- 위키링크, 백링크, 그래프 탐색
- 파일 변경은 승인 기반으로 처리되는 AI 워크플로우
- Tauri 기반 네이티브 런타임 (Electron 아님)

## 빠른 시작

```bash
pnpm install
pnpm --filter @kuku/desktop tauri:dev
```

## 레포지토리 구조

```text
apps/
  desktop/     Tauri 데스크톱 앱 (SolidJS + Rust)
  web/         Astro 웹 (랜딩/인증/대시보드)
  server/      Go API 서버 (Connect RPC)
crates/
  kuku-ai/       AI 연동
  kuku-contract/ RPC 계약 (Rust)
  kuku-indexer/  파일 인덱싱
packages/
  contract/    공유 계약 (gen/go + gen/ts)
infra/docker/
  local/       로컬 스택 (web + server + postgres + mailpit)
  preview/     스테이징
  prod/        프로덕션
```

## 기여

이슈/PR 환영합니다. 큰 변경은 먼저 이슈로 논의해주세요.

## 라이선스

[MIT](LICENSE) © kuku-mom
