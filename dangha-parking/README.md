# 당하동 1250 주차전용건축물 — 분양성 검토 (산출물 안내)

검단신도시 당하동 1250(P2-주9) 주차전용건축물의 **분양 가능성·적정 분양가** 중심 검토.
범위: 입지·개발호재·주변 시세·직접 비교사례·가격형성·**추천 분양 평단가**(+주차 운영단가 참고).
사업수지(수입·지출 손익·가능여부) 판정은 범위 밖 — 다음 단계.

## 산출물
| 파일 | 설명 |
|---|---|
| `report.html` → `당하동_주차전용건축물_분양성검토_보고서.pdf` | 가로 16:9 발표형 보고서(12장, SSOT=HTML) |
| `deck.html` → `당하동_주차전용건축물_사업성검토_발표자료.pdf` | 가로 16:9 요약 발표자료(13장) |
| `map_locator.png` / `map_locator.html` | 위치도(정적 PNG / 렌더 원본) |
| `map_locator_edit.html` | **위치도 핀 드래그 보정 도구**(아래 5% 참고) |
| `dwg_site_a102.png` · `dwg_floor1_a202.png` | 배치도·1층 평면도 |
| `당하동_주차장부지_개발_도면.pdf` | 원자료 소스 도면 |

> HTML이 원본(SSOT), PDF는 파생물. **수정은 항상 HTML에서** 하고 PDF를 재생성한다.

## 디자인
그래파이트 네이비 + 골드 강조(파랑 절제). 표지 배경에 `cover_render.png` 슬롯(실사 렌더용) — 미제공 시 블루프린트 텍스처 폴백.
**다방(Dabang) 디자인 규율 반영:** ① **Pretendard Variable** 단일 패밀리(세리프 제거) — 위계는 크기보다 굵기·위치로 ② **box-shadow 0** — 깊이는 1px 헤어라인(`#dfdfdf`) + 배경 톤(`#f5f5f5`)으로만 ③ 3계층 색 규율 — 골드=브랜드/강조, 회색=콘텐츠, 파란 틴트 제거(근생 경로 카드도 골드 틴트로 통일).

## ⏳ 남은 작업(사용자 몫, 약 5%)
1. **표지 실사 렌더 이미지** — `cover_render.png`(가로 16:9, 1600×900↑)를 이 폴더에 넣으면 표지에 자동 합성.
   - 프롬프트: *Photorealistic architectural rendering of a modern 5-story parking-and-retail building in a Korean new town (검단신도시), dusk, glass-and-metal facade, warm-lit ground-floor retail, 3-sided street frontage, ㄷ-shaped massing. Building on the RIGHT; LEFT third dark sky for text. Muted graphite & navy with warm light, subtle gold. 16:9, cinematic. No text.*
2. **위치도 ①대상지·②K타워 필지 정밀점** — 현재 "인근 블록 추정"(아라역·법조타운·법조타워는 OSM 검증 좌표로 확정). `map_locator_edit.html`을 브라우저로 열어 ①②만 정확한 건물로 드래그 → [좌표 복사] → 전달하면 확정 반영.

## PDF 재생성 (Windows Chrome 헤드리스)
```bash
chrome --headless=new --disable-gpu --no-pdf-header-footer \
  --print-to-pdf=OUT.pdf --virtual-time-budget=15000 file:///.../report.html
```
한글 경로 이슈 시 HTML+이미지를 ASCII 임시폴더에 복사 후 렌더.
