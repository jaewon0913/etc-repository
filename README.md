# 마크다운 작성요령

## 1. Headers(헤더)
- `<h1> ~ <h6>` 까지 가능하다.
```
# This is a h1 tag
## This is a h2 tag
##### This is a h5 tag
```
---
# This is a h1 tag
## This is a h2 tag
##### This is a h5 tag
---

## 2. Horizontal Rule(수평선)
- 아래 코드들 모두 사용 가능하다.
```
---
***
___
******
```
---
***
___
******

## 3. Line Breaks(줄바꿈)
```
  (띄어쓰기 두번)
<br/>
```

## 4. Emphasis(강조)
- 사용하고자 하는 부분에 붙여서 사용한다.
```
_Italic(이탤릭)_ or *Italic(이텔릭)*
**굵은 글씨(bold체)**
~~취소선~~
<u>밑줄</u>
ex) 이것은 _**마크다운**_ 글 강조 <u>**작성**</u> 가이드 ~~입니다.~~
```
***
_Italic_  / *이텔릭체*  
**굵은 글씨(bold체)**    
~~취소선~~  
<u>밑줄</u>  
ex) 이것은 _**마크다운**_ 글 강조 <u>**작성**</u> 가이드 ~~입니다.~~
***

## 5. BlockQuote(인용문)
- `>` 블럭 인용 문자를 사용하면 인용문 표현이 가능하다.
```
> 인용문장
>> 중첩 인용문
>>> 다중첩된 인용문
```
---
> 인용문장
>> 중첩 인용문
>>> 다중첩된 인용문
---

## 6. Lists(목록)
### 6-1. 순서가 필요없는 목록
- (+, -, *) 지원하며, 혼합 가능하다.
```
- Item 1
* Item 2
  - Item a
  - Item b
```
---
- Item 1
* Item 2
    - Item a
    - Item b
---
### 6-2. 순서가 필요한 목록
- 번호로 작성이 가능하다.(1로만 작성하여도 가능)
```
1. Item 1
1. Item 2 (= 2. Item 2)
1. Item 3 (= 3. Item 3)
   1. Item a
   1. Item b
```
---
1. Item 1
1. Item 2 (= 2. Item2)
1. Item 3 (= 3. Item3)
    1. Item a
    1. Item b
---

## 7.Links(링크)
```
1. 기본: [대체텍스트](URL)
여기를 클릭하세요: [블로그로 이동](https://dev-jwblog.tistory.com/)
2. 일반URL 작성 시 자동으로 생성
https://dev-jwblog.tistory.com/
```
***
1. 여기를 클릭하세요: [블로그로 이동](https://dev-jwblog.tistory.com/)
2. https://dev-jwblog.tistory.com/
***

## 8.Images(이미지)
- 링크와 유사하지만 앞에 `!` 가 붙는다.
### 8-1. 기본 사용법
```
1. ![대체텍스트](이미지경로)
2. <img alt="대체텍스트" src="경로" width="300" height="300"></img>
```
---
![jaewon](resources/images/jaewon_profile.jpg)  
<img alt="jaewon" src="resources/images/jaewon_profile.jpg" width="300" height="300"></img>
---
### 8-2. 혼합 사용법
- 링크와 이미지를 같이 사용할 수 있다.
```
[![대체텍스트](이미지경로)](URL)
[![jaewon](/resources/images/jaewon_profile.jpg)](https://dev-jwblog.tistory.com/)
```
---
- 클릭하면 블로그로 이동하게 됩니다.  
[![jaewon](/resources/images/jaewon_profile.jpg)](https://dev-jwblog.tistory.com/)
---

## 9. Code(코드)
### 9-1. Block Code(블록코드)
- 기본적으로는 ` ``` 내용작성 ``` `을 사용한다.
- 코드를 명시하여 style 에 맞게 사용가능하다.(` ``` java 내용작성 ``` `)
#### a. 기본
````
```
<a href="https://dev-jwblog.tistory.com/" title="블로그이동">블로그</a>
```
````
```
<a href="https://dev-jwblog.tistory.com/" title="블로그이동">블로그</a>
```
#### b. 코드타입 정의
````
``` html
<a href="https://dev-jwblog.tistory.com/" title="블로그이동">html 형식</a>
```
````
``` html
<a href="https://dev-jwblog.tistory.com/" title="블로그이동">html 형식</a>
```

````
``` css
div {
  color : red;
}
```
````
``` css
div {
  color : red;
}
```

````
``` javascript
console.log("javascript")
```
````
``` javascript
console.log("javascript")
```

````
``` java
String text = "java";
```
````
``` java
String text = "java";
```

### 9-2. Inline code(인라인코드)
```
사용법: `텍스트` 를 작성합니다.
```
---
사용법: `텍스트` 를 작성합니다.

---

## 10. Table(표)
- `|`(Vertical Bar) 기호를 사용하여 테이블을 표현한다.
- `:`(콜론) 기호를 통해 정렬할 수 있다.
- 헤더와 셀을 구분할 때 3개 이상의 `- 또는 :`가 필요 하다.
```
| Header | value | Description |
| --: | :-- | :--: |
| 정렬방법 | --: | 우측정렬 |
| 정렬방법 | :-- | 좌측정렬 |
| 정렬방법 | :--: | 가운데정렬 |
```
---
| Header | value | Description |
| --: | :-- | :--: |
| 정렬방법 | --: | 우측정렬 |
| 정렬방법 | :-- | 좌측정렬 |
| 정렬방법 | :--: | 가운데정렬 |
---

## 11. Syntax highlighting(구문 강조)
````
```js:index.js
function helloAlert(arg) {
  if (arg) {
    console.log("hello");
  }
}
```

```java:main.java
public static void main(String[] args){
  String hello = "hello";
  System.out.println(hello);
}
```
````
---
```js:index.js
function helloAlert(arg) {
  if (arg) {
    console.log("hello");
  }
}
```
```java:main.java
public static void main(String[] args){
  String hello = "hello";
  System.out.println(hello);
}
```
---

## 12. Task Lists(체크 목록)
```
- [x] 할일 완료
- [ ] 할일 미완료
```
***
- [x] 할일 완료
- [ ] 할일 미완료
***

## 13. Raw HTML(원시 HTML)
- 마크다운에서는 순수 HTML 형식도 가능하다.
```
<img alt="jaewon" src="resources/images/jaewon_profile.jpg" width="300" height="300"></img>
이글은 <span style="color:red">마크다운</span> 가이드입니다.
```
---
이글은 <span style="color:red">마크다운</span> 가이드입니다.

---