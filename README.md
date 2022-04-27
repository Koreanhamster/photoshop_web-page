photoshop_web-page
===
 URL: https://koreanhamster.github.io/photoshop_web-page/
 <img width="1025" alt="Screen Shot 2022-04-27 at 11 38 08 PM" src="https://user-images.githubusercontent.com/95600994/165543890-8b156d82-caf5-4835-b47e-5202186a816b.png">

## 기술 스택
- HTML
- CSS

## 신경쓴 점
- 네거티브 마진을 적극적으로 사용하여 자유롭게 박스포지셔닝을 할 수 있도록 했다.
- 아래 코드와 같이 nth-child속성을 사용하여 두 박스가 항상 중간 여백을 유지할 수 있도록 했다.

```html
.main {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 7rem 0;
}

.card:nth-child(odd) {
  margin-left: -60%;
}

.card:nth-child(even) {
  margin-left: 60%;
}
```
- 가상요소를 적극적으로 사용하여 박스 옆 말꼬리, 말꼬리 옆의 작은 원들을 구현하였다.
```html
.card:nth-child(odd)::before {
  content: '';
  position: absolute;
  display: block;
  border: 3px solid #1c90ff;
  background-color: #222;
  width: 0.8rem;
  height: 0.8rem;
  border-radius: 50%;
  top: 47%;
  right: -1.6rem;
  z-index: 50;
}

.card:nth-child(even)::before {
  content: '';
  position: absolute;
  display: block;
  border: 3px solid #1c90ff;
  background-color: #222;
  width: 0.8rem;
  height: 0.8rem;
  border-radius: 50%;
  top: 47%;
  left: -1.6rem;
  z-index: 50;
}
```
<img width="350" alt="Screen Shot 2022-04-27 at 11 46 31 PM" src="https://user-images.githubusercontent.com/95600994/165545985-8bd9cd96-8071-4094-bac9-b8ee9e321bd6.png">
(가상요소로 구현하여 위치를 지정한 파란 원과 화살 표시)

## 배운 점, 아쉬운 점
- challenge로 시작한 작업이라 그런지 정말 요소 하나하나, 배치 하나하나가 고민의(고난의) 연속이었다.
- 중간에 가상요소에 display:block을 지정하지 않아 한참을 헤메었다. 가상요소=display:block은 항상 따라다니는 짝꿍이다. 기억하자!
- absolute를 연습하기 위해 많이 사용을 했지만 역시 끝날때 쯤 가니 내가 CSS를 컨트롤 하고있다기 보다는 하나만 먹혀라 식으로 하고있는 내 자신을 발견했다. 계속해서 수양이 필요하다.
- 

 
