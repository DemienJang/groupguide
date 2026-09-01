# 보배마을 소그룹 가이드 HTML 제작 지침

이 프로젝트에서 새 소그룹 가이드 HTML 문서를 만들 때는 기존 `group-guide` 폴더의 최신 HTML 파일을 템플릿으로 삼는다.

## 기본 원칙

- 기존 HTML 템플릿의 구조, CSS, 클래스명, 반응형 규칙, 인쇄 스타일, 하단 빠른 이동 메뉴, 전체 시각 톤을 최대한 그대로 유지한다.
- 레이아웃을 새로 디자인하지 않는다.
- 색상, 카드 스타일, 버튼 스타일, 섹션 헤더, 토글, 질문 박스, 교사 멘트, 학생 답변 예시, 교사 포인트 같은 기존 구성 요소를 그대로 활용한다.
- 새 주제에 맞게 텍스트와 필요한 반복 블록만 교체한다.
- 새 UI 패턴을 만들기보다 기존 블록을 조합한다.

## 문서 구조

기본 구조는 기존 가이드의 흐름을 따른다.

1. 설교 한 눈에 보기
2. 설교 핵심 흐름
3. 필요 시 추가 성경지식 또는 배경 섹션
4. 본문과 학생 이해
5. 교사가 먼저 붙잡을 원칙
6. 소그룹 나눔 진행 가이드
7. 이럴 때 이렇게
8. 교사를 위한 묵상

필요할 경우 새 구역을 추가할 수 있다. 단, 새 구역도 기존 섹션 규칙을 따른다. 섹션 번호, `section-head`, `badge-num`, `card`, `grid`, `details`, `activity-card` 등 기존 클래스와 문서 톤을 활용한다.

## 내용 작성

- 내용은 새 설교 주제에 맞게 자연스럽게 작성한다.
- 기존 문장을 기계적으로 복사하지 말고, 설교의 본문, 핵심 메시지, 학생들의 실제 삶, 교사가 조심해야 할 지점에 맞춰 새롭게 구성한다.
- 말투는 기존 가이드처럼 정중하고 따뜻한 교사용 안내문 톤을 유지한다.
- 소그룹 질문은 학생들이 부담 없이 말할 수 있도록 구성한다.
- 필수 질문은 보통 3개, 선택 질문은 1개 정도로 둔다.
- 각 질문에는 가능하면 질문 의도, 학생 답변 예시, 진행 멘트, 교사 포인트를 함께 넣는다.

## 성경지식 섹션

성경지식 섹션을 넣을 때는 교사가 바로 설명할 수 있도록 쉬운 언어로 풀어 쓴다.

- 어려운 신학 용어는 정의, 의미, 학생용 설명, 연결 성경 구절 순서로 정리한다.
- 연결 구절은 성경 본문을 직접 인용한다.
- 각 용어는 `<details open><summary>용어</summary>...</details>` 형태의 토글 블록으로 만든다.
- 사용자가 따로 요청하지 않는 한 헬라어 원어 표기는 넣지 않는다.

## OG 메타데이터

모든 새 HTML 문서에는 OG 메타데이터를 넣는다. OG 이미지는 항상 동일하게 아래 주소를 사용한다.

```html
<meta property="og:image" content="https://groupguide.vercel.app/images/group-guide.jpg">
<meta property="og:image:alt" content="보배마을 소그룹 나눔 가이드">
```

새 문서에는 최소한 다음 OG 정보를 포함한다.

```html
<meta property="og:title" content="문서 제목 · 교사용 소그룹 나눔 가이드">
<meta property="og:description" content="새 문서의 핵심 설명">
<meta property="og:type" content="website">
<meta property="og:url" content="https://groupguide.vercel.app/파일명.html">
<meta property="og:image" content="https://groupguide.vercel.app/images/group-guide.jpg">
<meta property="og:image:alt" content="보배마을 소그룹 나눔 가이드">
```

## 인덱스 업데이트

새 가이드를 만들면 `index.html`에도 추가한다.

- 최신 가이드는 상단 대표 카드로 올린다.
- 기존 최신 가이드는 해당 월 목록으로 내려보낸다.
- 월별 목록이 없으면 새 월 섹션을 만든다.
- 검색용 `data-search`에도 날짜, 제목, 본문, 핵심 주제, 소그룹 나눔 관련 키워드를 넣는다.

## 완료 기준

- 새 HTML 파일과 `index.html`을 확인한다.
- OG 이미지 경로가 `https://groupguide.vercel.app/images/group-guide.jpg`인지 확인한다.
- 사용자가 요청하면 변경사항을 커밋하고 `origin/main`으로 푸시한다.
