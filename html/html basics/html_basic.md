## 1. 강조 태그
1. em
2. strong

## 2. Anchor
href = hypertext reference 필수 속성

### hreft 주소값 표기 방법
* URL 표기법
```html
<a href='http://youtube.com'>Youtube</a>
```
* 페이지 내 이동
다른 이동하고자 하는 부분의 id를 작성해주면 됨
```
<a href='#title'>move to title</a>
```
* 메일 주소
```
<a href="mailto:wjinh93@gmail.com">나에게 메일 쓰기</a>
```
* 전화번호 (모바일에서 자주 사용)
```
<a href="tel:01012345678"> 나에게 전화걸기 </a>
```
### 속성
1. target
> 새로운 탭으로 열기

```html
<a href='http://youtube.com' target="_blank">Youtube</a>
```

## 3. Image

### alt (alternative text)
> 이미지가 뜨지 않을때 텍스트로 나타냄. 혹은 앞을 못보는 사람들을 위해 screen reader를 이용 할때 사운드로 알려줌.

## 4. List
## ol (ordered list)
>순서가 중요한 목록.
>ol만 있다고 리스트가 만들어지지 않음. 안에 list item의 약자인 li 태그가 필요

<strong>ul과 ol의 자식요소는 무조건 li만 가능</strong>

## ul (unordered list)
> 순서가 중요하지 않은 목록


## 5. Description List(정의 리스트)
> 1. 용어를 정의 할 때 사용
2. key-value로 정보를 제공할 때

* 주의 해야 할 점
dl의 자식요소는 오직 div, dt, dd 만 가능하다!

### dl
> dl을 선언하는 태그

### dt (description term)
> key값에 해당
> 여러개가 나올 수도 있음

```html
<dl>
<dt> 학습 </dt>
<dt> 배움 </dt>
<dd> 배워서 익히는일 </dd>
</dl>

```
### dd(description data)
> value값에 해당
> 여러개 일 일 수 도 있음.

```html
<dt> 
  <dfn> 학습 </dfn>
    </dt>
<dd>배워서 익히는일</dd>
<dd>배움은... </dd>

```

### dl의 잘못된 예시



```html
<dl>
  <dt>학습</dt>
  <dd>배워서 익히는 일</dd>
  <dt>배움</dt>
</dl>

<dl>
  <section>
    <dt>학습</dt>
    <dd>배워서 익히는 일</dd>
  </section> 
</dl>
```

## 6. 인용

### blockquote
> 들여쓰기가 생기고 blockquote를 썼을 때 저자가 인용한것을 가져왔구나라는걸 브라우저로 하여금 알게 하는것


### cite
> 인용한 문구의 출처를 남길 때 사용하는 태그

만약 url 출처를 남기고 싶을때는 blockquote 옆에 cite='url'주소를 작성하면 된다.
![](https://images.velog.io/images/jin0106/post/742f73d8-3008-46dd-a6b7-969722f995ff/image.png)

### q 태그
> 문장내에 살짝 들어가는 인용문을 작성 할 때 사용 