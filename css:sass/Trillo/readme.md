# Trillo: A Flexbox Project

* 두번째 CSS and SASS Project. 
* 메인 목표: Flex를 사용하여 반응형 웹 페이지 만들기
* Flex 이외에도 SVG icons, BEM, animations, CSS Variables 등을 활용하기

## Instructions

프로젝트를 다운 받은뒤 아래를 실행하면 된다

```javascript
npm install
npm start
```



## CSS Custom Properties

* `<html>` 요소를 대표하는 `:root` 가상요소에 변수들을 아래와 같이 정의 한다.

```scss
:root {
  --color-primary: #eb2f64;
  --color-primary-light: #FF3366;
  --color-primary-dark: #BA265D;
  --color-gray-light-1: #faf9f9;
  --color-gray-light-2: #f4f2f2;
  --color-gray-light-3: #f0eeee;
  --color-gray-light-4: #ccc;
  --color-gray-dark-1: #333;
  --color-gray-dark-2: #777;
  --color-gray-dark-3: #999;
  --shadow-dark: 0 2rem 6rem rgba(0, 0, 0, .3);
  --shadow-light: 0 2rem 5rem rgba(0, 0, 0, .06);
  --line: 1px solid var(--color-gray-light-2);
}
```

사용을 할때는 css 어디에서든 `var()` function으로 사용 할 수있다. `color: var(--color-primary)`





## SVG Icons vs Icon Fonts

SVG icons이 가지는 가장 큰 장점은 강력한 접근성이다. 스크린 리더에 접근할 수 있는 `<title>` `<desc>`와 같은 요소들을 가지고 있고, 아이콘에 색상을 지정할 수 있는 등 여러 애니메이션 옵션을 가지고 있다. 

또한 SVG는 브라우저가 이미지로 인식하기 때문에 쉽게 포지셔닝을 할 수 있다. 반면에 icon fonts들은 가상요소를 사용하여 위치를 이동시켜야 하기 때문에 비교적 어려울수도 있다.

`svg파일의 경로#해당 아이콘의 이름`

```html
<svg>
  <use xlink:href="img/sprite.svg#icon-map-pin"></use>
</sv>
```



## Useful websites

* <a href='https://icomoon.io'>iconMoon</a> : free vector icons 

* <a href="https://cubic-bezier.com">Cubic Bezier</a> : `cubic-bezier()`기능 제너레이터

* <a href="https://css-tricks.com/snippets/html/glyphs/">Glyphs</a> : CSS와 HTML에서 사용할 수 있는 glyphs 코드 참고 웹사이트

* <a href="http://getbem.com">BEM Methodology</a> : CSS code와 CSS class name을 쉽게 구성하는 법을 알려주는 웹 사이트

* <a href="https://tinypng.com">Tiny PNG</a> : PNG와 JPEG 파일 압축 해주는 사이트

  

