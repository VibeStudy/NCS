---
name: ncs-problem-completer
description: Complete missing parts of Korean NCS practice-problem Markdown files from the question context and referenced concept notes. Use when `문제유형/**/*.md` has incomplete choices, answer, 풀이, 보기, question text, or a partial marker such as `A.`, and the user asks to fill or finish it.
---

# NCS 문제 빈칸 완성

미완성 NCS 문제의 누락 부분만 참조 노트 근거로 완성한다.

공통 문항 양식은 저장소 `docs/problem-format.md`를 단일 기준으로 삼는다.

## 작업 순서

1. 파일 수정 전 저장소 `AGENTS.md`, `docs/format.md`, `docs/problem-format.md`를 읽는다.
2. 대상 문제 파일 전체를 읽고, 빈칸의 범위를 확인한다.
3. 과목명에 맞는 `note/` 문서를 찾거나 사용자가 지정한 참조 노트의 관련 단원을 읽는다.
4. 지문 조건과 노트 개념을 각각 대조해 정답을 확정한다.
5. 누락된 부분만 채우고, 기존에 완성된 지문·선지·정답은 바꾸지 않는다.

## 완성 규칙

* 불완전 표기 `A.`는 정답·풀이 양식으로 바꾼다.
* 선택지는 하나만 명확히 정답이 되게 만들고, 오답은 노트에 있는 다른 개념으로 구성한다.
* 지문만으로 정답을 확정할 수 없고 노트에도 근거가 없으면 내용을 추정하지 말고 사용자에게 확인을 요청한다.

## 문항 예제

````markdown
Q. 다음 사례에서 요리연구가 A가 사용한 방법으로 가장 적절한 것은?

```
A씨는 요리 방법을 적은 문서를 분류해 책으로 출판하였다. 책은 주재료를 기준으로 요리 방법을 분류했으며, 각 재료의 내용이 있는 페이지도 함께 적었다.
```

① 자료 수집과 
② 분류와 색인
③ 요약과 편집
④ 검색과 공유
⑤ 정보 보안과 백업

정답: ②

풀이: 주재료를 기준으로 나눈 것은 분류이다. 재료명과 해당 페이지를 함께 적은 것은 색인이다.
````

## 검토

* `docs/problem-format.md`의 선지·정답·풀이 형식을 확인한다.
* 풀이가 정답의 직접 근거를 설명하는지 확인한다.
* 문제의 기존 형식, 단원 문항 수, 문항 사이 `---`를 확인한다.
