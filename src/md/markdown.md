# 마크다운 언어란?

> 문서를 쉽게 작성하고 가독성을 높이기 위해 개발된 **경량 마크업 언어**로, 간단한 문법을 사용하여 다양한 플랫폼을 지원한다는 특징을 가지며 README파일, 블로그, 기술 문서, 노트 등 다양한 목적으로 사용 됨

<br />

# 마크다운 문법 정리

## 1. 제목(Headers)

> 마크다운에서 제목을 작성하는 방식 2가지
>
> - `#`을 사용하는 ATX 스타일 방식
> - `=` 혹은 `-`을 사용하는 Setext 스타일 방식
>
>   ※ Setext 스타일은 주로 전통적인 문서 스타일에서 사용되며, 근래에는 ATX 스타일이 더 일반적임

### 1-1. ATX 스타일 (ATX-style) → `#` 기호 사용

- 사용법 : `#`\*n(1~6) + 제목
  - \#의 개수에 따라 제목의 크기가 결정됨
  - \#으로 헤더를 닫을 수도 있으나 필수가 아니며 닫지 않아도 상관 없음.
- 🤖사용 예시

  ```
  # Heading1
  ## Heading2
  ### Heading3
  #### Heading4
  ##### Heading5
  ###### Heading6
  ```

- ✅출력 결과

  # Heading1

  ## Heading2

  ### Heading3

  #### Heading4

  ##### Heading5

  ###### Heading6

### 1-2. Setext 스타일 (Setext-style) → `=`와 `-` 기호 사용

- 사용법 : 제목 아랫줄에 \=(H1) 혹은 \-(H2) 기호로 구분선을 배치
  - H1, H2만 지원되며 H3~H6은 사용할 수 없음
  - \= 또는 \-의 개수는 상관없지만, 적어도 3개 이상 넣어야 함
- 🤖사용 예시

  ```
  Heading1
  ===
  Heading2
  ---
  ```

- ✅출력 결과

  # Heading1

  ## Heading2

<br />

## 2.인용문(Blockquote)

> `>` 기호를 사용하여 인용문을 작성할 수 있음

- 사용법 : `>` \+ 인용하고 싶은 내용
- 🤖사용 예시

  ```
  > Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque deserunt enim necessitatibus accusantium sunt fugit delectus, quibusdam libero perferendis. Vero, tempora illum reprehenderit magnam voluptatibus temporibus ipsum pariatur molestias explicabo.

  > This is the first level of quoting.
  >
  > > This is nested blockquote.
  >
  > Back to the first level.
  ```

- ✅출력 결과

  > Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque deserunt enim necessitatibus accusantium sunt fugit delectus, quibusdam libero perferendis. Vero, tempora illum reprehenderit magnam voluptatibus temporibus ipsum pariatur molestias explicabo.

  > This is the first level of quoting.
  >
  > > This is nested blockquote.
  >
  > Back to the first level.

## 3. 목록(Lists)

> 마크다운에서는 순서 없는 목록과 순서 있는 목록을 각각 나타낼 수 있다.

### 3-1. 순서 없는 목록(Unordered List) → `-`, `*`, `+` 기호 사용

- 사용법 : 기호(`-`\,`*`\,`+`) \+ 항목
  - 하위 리스트는 여백(space bar) 세 칸 혹은 Tap 으로 구분함
- 🤖사용 예시
  ```
  * Red
    * Crimson Red
    * Scarlet  Red
  * Green
  * Blue
  ```
- ✅출력 결과
  - Red
    - Crimson Red
    - Scarlet Red
  - Green
  - Blue

### 3-2. 순서 있는 목록(Ordered lists) → 숫자\. 사용

- 사용법 : `숫자.` \+ 항목
  - 하위 리스트는 여백(space bar) 세 칸 혹은 Tap 으로 구분함
- 🤖사용 예시
  ```
  1. 첫 번째 항목
     1. 하위 항목1
     2. 하위 항목2
  2. 두 번째 항목
  3. 세 번째 항목
  ```
- ✅출력 결과

1. 첫 번째 항목
   1. 하위 항목1
   2. 하위 항목2
2. 두 번째 항목
3. 세 번째 항목

## 4. 링크(Links)

> 마크다운에서는 `inline`과 `reference`로 2가지 형식의 링크 기능을 제공

### 4-1. 인라인 링크(Inline Link) → 텍스트와 URL을 한 줄에 작성

- 사용법 : `[참조](링크)`
  - 짧은 문서를 작성할 때나, 적은 링크를 기재할 때 사용
  - 보기 쉽고 직관적이나 여러 번 같은 URL을 사용할 경우 중복 발생
- 🤖사용 예시
  ```
  [멋쟁이 사자처럼 부트 캠프](https://bootcamp.likelion.net/)
  ```
- ✅출력 결과  
  [멋쟁이 사자처럼 부트 캠프](https://bootcamp.likelion.net/)

### 4-2. 참조 링크(Reference Link) → 링크를 본문과 분리하여 따로 정의

- 사용법 :
  - `[참조][id]`  
    `[id]: 링크`
  - 긴 문서를 작성할 때나 동일한 URL을 반복적으로 사용할 때 유용
  - 링크를 한 곳에서 관리하여 유지보수가 쉬움
- 🤖사용 예시

  ```
  [멋쟁이 사자처럼 부트 캠프][likelion-link]
  [구글][google-link]

  [likelion-link]: https://bootcamp.likelion.net
  [google-link]: https://www.google.com
  ```

- ✅출력 결과  
  [멋쟁이 사자처럼 부트 캠프][likelion-link]  
  [구글][google-link]

  [likelion-link]: https://bootcamp.likelion.net/
  [google-link]: https://www.google.com

## 5. 강조(Emphasis)

> 마크다운에서는 굵게, 기울임, 취소선 등 다양한 형식의 글 스타일을 제공함

- 사용법
  | 스타일 | 사용법 |  
  | :----: | :------- |
  | 굵게(Bold) | `**`텍스트`**` 또는 `__`텍스트`__`|
  | 기울임(Italic) | `*`텍스트`*` 또는 `_`텍스트`_`|
  | 취소선(Strikethough) | `~~`텍스트`~~`|

- 🤖사용 예시

  ```
  **굵은 텍스트1**
  __굵은 텍스트2__
  *기울임 텍스트1*
  _기울임 텍스트2_
  ~~취소선~~
  ```

- ✅출력 결과  
  **굵은 텍스트1**  
  **굵은 텍스트2**  
  _기울임 텍스트1_  
  _기울임 텍스트2_  
  ~~취소선~~

## 6. .코드(Code)

- 사용법 : 한 줄은 `` ` ``코드`` ` ``, 여러 줄의 경우 ` ``` `코드 블록` ``` `
  - 문자 `` ` ``를 문장 안에 넣고 싶은 경우, 백틱 2개(` `` `)를 앞뒤에 삽입하여 표현 가능
  - 코드 블록의 경우, 시작 백틱 뒤에 **언어명**을 붙이면 해당 언어에 맞는 양식으로 보여줌
- 🤖사용 예시

  ````
  `print("Hello, World!")`
  ``There is a literal backtick (`) here.``

  ```
  def hello():
    print("Hello, World!")
  ```

  ```python
    def hello():
    print("Hello, World!")
  ```

  ````

- ✅출력 결과  
  `print("Hello, World!")`  
  ``There is a literal backtick (`) here.``

  ```
  def hello():
    print("Hello, World!")
  ```

  ```python
    def hello():
    print("Hello, World!")
  ```

## 7. 이미지(Images)

- 사용법 : `![대체 텍스트](이미지 주소 "(※선택적)설명")`
- 🤖사용 예시

  ```
  ![김지원 사진](/src/assets/images/jiwon.jpeg "정말 예쁜 김지원")
  ```

- ✅출력 결과

  ![김지원 사진](/src/assets/images/jiwon.jpeg "정말 예쁜 김지원")

## 8. 표(Tables)

- 사용법
  - `|` 사이에 컬럼명 기재, 내용 행과 컬럼행 사이를 `|---|`로 구분
  - 헤더 구분선에 `:` 기호로 정렬 구분 \/\/ `--:`\(우측 정렬\), `:--:`\(가운데 정렬\), `:--`\(좌측 정렬\)
- 🤖사용 예시

  ```
  | 이름 | 나이 | 직업 |
  | :--: | :--: | :-- |
  | 코난 | 7세 | 탐정 |
  | 지우 | 10세 | 포켓몬 챔피언|

  ```

- ✅출력 결과
  | 이름 | 나이 | 직업 |
  | :--: | :--: | :--: |
  | 코난 | 7세 | 탐정 |
  | 지우 | 10세 | 포켓몬 챔피언|

<br />

# 마크다운 문서 작성 시 유의점

- Enter로 여러 줄바꿈을 할 수 없음. 줄바꿈을 적용하려면 공백 2개 또는 `<br />` 태그를 사용
- 일부 특수 문자에 대한 자동 처리 주의 (`<` 와 `&`)
  - 태그를 시작하는데 사용되는 `<` 대신, 오류 방지를 위해 `&lt;` 를 사용하여 작성
  - `&` 는 HTML 엔티티의 시작을 나타내는데 사용됨. `&amp;`를 사용하여 작성
- `*`, `` ` `` 등 태그로 사용되는 특수 문자를 글에 사용하고 싶은 경우, 백슬래시\(`\`\)를 앞에 기재하여 적용할 수 있음
  - 마크다운에서 백슬래시 이스케이프를 제공하는 문자 목록
  - | 문자 |     Description     |          한글명           |
    | :--: | :-----------------: | :-----------------------: |
    |  \   |      backslash      |         백슬래시          |
    |  `   |      backtick       |      백틱(역따옴표)       |
    |  \*  |      asterisk       |    별표(애스터리스크)     |
    |  \_  |     underscore      |     밑줄(언더스코어)      |
    |  {}  |    curly braces     |          중괄호           |
    |  []  |   square brackets   |          대괄호           |
    |  ()  |     parentheses     |          소괄호           |
    |  #   |      hash mark      |      샵/해시/우물 정      |
    |  +   |      plus sign      |    더하기 기호/플러스     |
    |  -   | minus sign (hyphen) | 빼기 기호/마이너스/하이픈 |
    |  .   |         dot         |      점/마침표/도트       |
    |  !   |  exclamation mark   |          느낌표           |

<br />

# 출처

1. **Daring Fireball** - 마크다운 공식 문서

   - https://daringfireball.net/projects/markdown/

2. **유튜브 드림코딩** - 마크다운(Markdown) 6분 순삭 정리 + 깃허브 리드미(ReadMe) 파일 작성 팁

   - https://youtu.be/kMEb_BzyUqk?si=ayquCIXvP8ewF3sT
