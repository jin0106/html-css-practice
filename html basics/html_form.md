# Form
<hr>

꼭 필요한 2가지 : action, method

action = "API주소"
method = "GET | HOST"

## 1. GET 이란?
> 서버로부터 정보를 조회하기 위해 설계된 메소드.

* GET은 요청을 전송할 때 필요한 데이터를 Body에 담지 않고, 쿼리스트링을 통해 전송.
  * URL 끝에 `?`와 함게 이름과 값의 쌍을 이루는 요청 파라미터를 쿼리스트링이라 한다.
  * 만약 요청 파라미터가 여러개이면 `&`로 연결한다.

> www.example-url.com/resources?name1=value1&name2=value2

## 2. POST 

> 리소스를 생성/변경하기 위해 설계 되었다.

* GET과 달리 전송해야할 데이터를 HTTP 메시지의 Body에 담아 전송.
* HTTP 메시지의 Body는 길이 제한 없이 데이터 전송 가능. 그리하여 GET과 달리 대용량 데이터 전송 가능.
* 내용이 눈에 보이지 않아 GET보다 안전하다고 생각할 수 있지만 크롬 개발자도구 같은 툴로 확인 가능하기에 민감한 데이터의 경우에는 반드시 암호화해 전송해야한다. (csrf_token)

참고 : https://hongsii.github.io/2017/08/02/what-is-the-difference-get-and-post/


## 3. Input
### Type 종류
* text
* email
* password
* url
* number
  * min='12' max='122' attribute 사용 가능
* file
  * `accept='.png, .jpg'` png와 jpg파일만 업로드 가능 

### attribute

* placeholder
* maxlength, minlength : 최고 길이, 최저 길이 설정
* require : 이 속성이 있으면 필수로 입력해야함
* disabled : 사용 할 수 없게 막는것
* value : 일종의 초기 값. 아무것도 입력하지 않아도 들어가있음
```html
<form action='' method='GET'>
  <input type='text' placeholder='type your id' minlength='5' maxlength='13' requried>
</form>
```


## 4. label
> 특정 input에 대한 이름

`<label for='input id'>라벨 </label>`

## 5. Radio
![](https://images.velog.io/images/jin0106/post/44d26368-a30b-455a-bec4-d7d0eff77f63/image.png)

위와 같이 작성하면 두개 다 클릭이 됨. 왜?
name을 설정하지 않았기 때문에. 2개 중에 한개만 클릭되게 하려면 둘의 name을 동일하게 설정해줘야 한다. 선택시 name이 서버에 전달됨. 하지만 둘의 name이 같다면 뭐가 선택되었는지 모르기에 value를 설정해줘야한다.
![](https://images.velog.io/images/jin0106/post/2be2483e-a899-455c-bdd5-046b0b369c4f/image.png)


## 6. Select
```html
<label for='skill'> Skill </label>
<select name="skill" id="skill">
  <option value='html'> HTML </option>
  <option value='css'> CSS </option>
  <option value='js'> JS </option>
</select>
```

css를 선택시 url주소/?skill=css 이렇게 전송이 됨.
selct에 multiple attribute을 넣으면 여러개 선택이 됨.

## 7. Textarea
row와 cols로 크기 조절 가능

```html
<textarea row="30" cols="50"></textarea>
```


## 8. button
* button type 종류
	1.  button
	2. submit : form 을 제출하는 용도로 사용
    3. reset : 작성 했던것을 다시 작성하고 싶을때.
  
 ```html
<button type="reset"> 다시 쓰기 </button>