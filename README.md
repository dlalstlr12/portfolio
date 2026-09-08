# 이민식 — 백엔드 개발자 포트폴리오

정적 HTML 한 장으로 만든 포트폴리오 페이지입니다. 빌드 단계 없이 `index.html` 하나만 서빙합니다.

**Live** — https://portfolio-tau-tawny-ycw9588fg9.vercel.app

## 구성

```
index.html    # 전체 페이지 (HTML · CSS · 인라인 SVG, 외부 의존성은 웹폰트뿐)
vercel.json   # Vercel 정적 배포 설정
```

- 프레임워크·번들러 없음 → 빌드 시간 0, 유지보수 지점 1곳
- 다크 모드 대응 (`prefers-color-scheme`)
- 인쇄 스타일 포함 — 브라우저에서 `Ctrl/Cmd + P` → **PDF로 저장** 하면 제출용 PDF가 그대로 나옵니다
- 아키텍처 다이어그램은 인라인 SVG (이미지 요청 없음, 인쇄 시 선명)

## 로컬 확인

`index.html` 을 브라우저로 열면 끝입니다. 굳이 서버가 필요하면:

```bash
npx serve .
```

## 배포 (Vercel)

Framework Preset은 **Other**, 빌드 명령·출력 디렉터리는 비워두면 됩니다.

## PDF 뽑기

1. 브라우저에서 페이지 열기
2. `Ctrl/Cmd + P`
3. 대상: **PDF로 저장** / 용지: **A4** / 여백: **기본** / **배경 그래픽** 체크
