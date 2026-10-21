# jelly-icon-studio

유광 젤리 3D 아이콘을 **언제 생성하든 같은 세트로** 보이게 유지하기 위한 작업 기준 저장소입니다.

이 README는 AI(Claude / ChatGPT 등)가 읽는 작업 지침서입니다. "강아지 하네스", "고양이 숨숨집", "왕관"처럼 사물과 버전만 자연어로 요청받으면 아래 순서를 그대로 따르세요.

---

## 저장소 구조

```
CLAUDE.md                      클로드 코드가 자동으로 읽는 시작 지침
REGISTER.md                    새 아이콘 등록 자동화 (엘리먼트 & Figma & 깃허브)
style/
  JELLY_Style_Lock.md          범용 스타일 락 (항상 적용)
versions/
  JELLY_Cat_Version.md         고양이 버전 (핑크 & 발바닥)
  JELLY_Dog_Version.md         강아지 버전 (틸 & 뼈다귀)
  JELLY_Common_Version.md      공통 버전 (핑크 & 틸 포인트, 동물 모티프 없음)
characters/
  JELLY_Characters.md          캐릭터 몽실이 & 방실이 (고정 컬러, 얼굴 락)
library/
  JELLY_Object_Library.md      이미 만든 사물의 형태 묘사 사전
references/
  characters/                  캐릭터 레퍼런스 (항상 첨부)
    Mongsil_Front.png / Mongsil_4View.png
    Bangsil_Front.png / Bangsil_4View.png
  cat/                         고양이 아이콘 14종 정면컷 & 4뷰
  dog/                         강아지 아이콘 8종 정면컷 & 4뷰
  common/                      공통 아이콘 18종 정면컷 & 4뷰 (가격표 & 장바구니 & 쿠폰 시트는 4뷰 없음)
                               → 사물별 파일명은 library/JELLY_Object_Library.md의 Reference image map
```

---

## 작업 순서

### 1. 스타일 락 로드 (필수 & 예외 없음)

모든 아이콘 요청은 `style/JELLY_Style_Lock.md`를 먼저 읽는 것으로 시작합니다.
사물, 버전, 용도와 무관하게 항상 적용됩니다.

### 2. 버전 파일 판단

요청 내용에 따라 `versions/` 파일을 하나만 추가로 읽습니다.

| 요청 키워드 | 적용 파일 |
|---|---|
| 고양이, 냥이, 캣 | `versions/JELLY_Cat_Version.md` |
| 강아지, 댕댕이, 개 | `versions/JELLY_Dog_Version.md` |
| 공통, 서비스 / 쇼핑 & 혜택 & 결제 & 배송 & 알림 & 일정 사물 | `versions/JELLY_Common_Version.md` |
| 버전 언급 없음 | `library/JELLY_Object_Library.md`의 고정 버전을 따름 |

펫용품인데 종 구분이 없고 라이브러리에도 고정 버전이 없으면, 버전을 정하지 말고 사용자에게 강아지인지 고양이인지 물어보세요.

### 2-1. 캐릭터 & 조합 판단

- 요청에 **몽실이** 또는 **방실이**가 있으면 `characters/JELLY_Characters.md`를 읽고 `references/characters/`의 해당 이미지를 반드시 첨부합니다.
  - 몽실이 = 크림색 + 오른쪽 귀 & 이마에 캐러멜 브라운 무늬 (고양이 그룹)
  - 방실이 = 무늬 없는 화이트 (강아지 그룹)
  - 캐릭터는 버전 컬러(핑크 & 틸)를 따르지 않습니다.
- "장바구니 안에 쿠폰, 몽실이, 선물상자"처럼 여러 아이콘을 한 장에 담는 요청은 `style/JELLY_Style_Lock.md`의 **Combination rule**을 따릅니다.
  - 담는 그릇(장바구니, 카트, 상자, 그릇 등) 1개 + 아이템 최대 3개
  - 각 아이템은 등록된 디자인 그대로 (버전 컬러는 그 아이템 기준)
  - 레퍼런스는 최대 4장: 그릇 1장 + 아이템마다 1장

### 3. 배경 판단

| 요청 키워드 | 배경 |
|---|---|
| 언급 없음 | **블랙** (기본) — 순수 블랙 + 버전 컬러 glow |
| 흰 배경, 화이트 배경, white | **화이트** — 순수 화이트 + 버전 컬러가 살짝 섞인 짧은 접지 그림자 |

배경만 바뀌고 재질 & 컬러 & 모티프 & 조명 & 구도는 그대로입니다. 세부 규칙은 `style/JELLY_Style_Lock.md`의 **Background options**를 따릅니다.
화이트로 만들어도 레퍼런스는 같은 버전 폴더의 블랙 이미지를 그대로 첨부합니다.

### 4. 사물 묘사

- `library/JELLY_Object_Library.md`에 있는 사물이면 그 영어 묘사를 **그대로** 씁니다.
- 없는 사물이면 영어 한 문장으로 새로 씁니다. 실제 사물을 장난감처럼 단순화하고, 알아볼 수 있는 부품 2~4개만 넣습니다. 컬러 & 재질 & 조명 & 배경 단어는 넣지 않습니다 (락과 버전 파일이 담당).

### 5. 레퍼런스 이미지 첨부

등록된 사물이면 `library/JELLY_Object_Library.md`의 **Reference image map**에서 그 사물의 정면컷을 첨부합니다. 새 사물이면 같은 버전 폴더에서 형태가 가장 비슷한 이미지를 첨부합니다.

| 생성 단계 | 첨부 |
|---|---|
| 정면컷 | 같은 버전 `*_Front.png` 1~2장 |
| 4뷰 시트 | 방금 만든 정면컷 1장 (필수) + 같은 버전 `*_4View.png` 1장 |

한 번에 첨부하는 이미지는 3장을 넘기지 않습니다.

### 6. 프롬프트 조립 & 전달

`style/JELLY_Style_Lock.md`의 **Prompt assembly** 순서대로 정면컷 프롬프트와 4뷰 프롬프트를 만들고, 엘리먼트 이름과 함께 전달합니다.

- 엘리먼트 이름: 공통은 `사물명`, 펫용품은 `사물명_고양이` / `사물명_강아지`
- 이미지 생성은 기본 Low 품질 & 최저 해상도 & 1장. 자동으로 여러 장 생성하거나 재생성하지 않습니다.

---

## 우선순위

충돌이 생기면 위쪽이 항상 이깁니다.

1. `style/JELLY_Style_Lock.md`
2. 첨부된 `references/` 이미지
3. `characters/JELLY_Characters.md` (캐릭터가 있을 때)
4. `versions/` 버전 파일
5. `library/` 사물 묘사
6. 사용자의 요청 (사물, 세부 형태)

요청이 스타일과 충돌하면 (예: "매트한 느낌으로", "카페 배경 넣어서", "그라데이션 배경으로") **스타일을 지키고**, 무엇을 조정했는지 사용자에게 알립니다.

---

## 금지 사항

- 락 파일 내용을 임의로 해석 & 완화 & 생략하지 않습니다.
- 사물 분위기에 맞춰 스타일을 바꾸지 않습니다. 사물이 바뀌어도 같은 젤리 세트입니다.
- 버전 컬러를 섞지 않습니다. 고양이 = 핑크 & 발바닥, 강아지 = 틸 & 뼈다귀.
- 4뷰 시트를 정면컷 없이 텍스트만으로 생성하지 않습니다.
- 락 파일(`style/`, `versions/`)은 사용자가 명시적으로 요청할 때만 수정합니다.

---

## 새 아이콘 추가 방법

새 아이콘이 최종 확정되면 `REGISTER.md`를 따릅니다. Higgsfield 엘리먼트 등록, Figma 정리, 깃허브 반영까지 한 번에 진행됩니다. 깃허브 부분만 요약하면:

1. `library/JELLY_Object_Library.md`의 해당 버전 표에 한 줄 추가 (사물명, 별칭, 기호, 영어 형태 묘사)
2. 대표성이 있으면 `references/{버전}/`에 `{Object}_Front.png`, `{Object}_4View.png` 추가
3. 이 README의 저장소 구조에 추가한 레퍼런스 반영

## 새 버전 추가 방법

새 버전(예: 시즌 한정 레드, 프리미엄 골드)을 추가할 때:

1. `versions/JELLY_{이름}_Version.md` 생성
   - 상단에 "`style/JELLY_Style_Lock.md`를 먼저 읽을 것, 락 파일이 상위 우선순위" 명시
   - 컬러 & 모티프 & glow만 정의. 재질 & 조명 & 구도 & 형태는 건드리지 않음
   - 이 버전을 쓰지 말아야 할 상황도 함께 기재
2. `references/{이름}/`에 정면컷 & 4뷰 레퍼런스 추가
3. 이 README의 구조 & 버전 판단 표에 항목 추가
