# starbucksDema
# Library
### lodash cdn
### gsap cdn
### swiperjs
### Youtube IFrame API
### ScrollMagic cdn

# ご覧になる方法

![2](https://user-images.githubusercontent.com/61581807/115183963-c9fc3180-a117-11eb-864d-5f92721d9798.png)


ダウンロードにした圧縮ファイルの解凍をしてください。



![3](https://user-images.githubusercontent.com/61581807/115184098-16e00800-a118-11eb-8c93-c1d0d7e5ab86.png)



# 2021-04-23 (git branch, signin)

branch 추가

git branch
git branch signin
git checkout signin
git add .
git commit -m ''

# 2021-04-23(footer, html entities, ScrollTo)



![image](https://user-images.githubusercontent.com/61581807/115820708-5ec69e00-a43c-11eb-90a3-8b0989bbc0d4.png)


![image](https://user-images.githubusercontent.com/61581807/115841838-2a60db00-a458-11eb-843d-8edc596e6a20.png)



# 2021-04-22(medal(3D animation), ScrollMagic cdn)

```
// ScrollMagic

const spyEls = document.querySelectorAll('section.scroll-spy');

spyEls.forEach(function(spyEl){
  new ScrollMagic
  .Scene({
    triggerElement: spyEl, // 보여짐 여부를 감시할 요소를 지정
    triggerHook: .8 // top 0 , bottom 1 사이에 가상의 선을 지정
  })
  .setClassToggle(spyEl, 'show') // triggerHook의 선을 넘으면 해당 클래스에 show를 붙인다
  .addTo(new ScrollMagic.Controller());
});

```

![123](https://user-images.githubusercontent.com/61581807/115682966-ece54a80-a390-11eb-8f35-42651e9e7913.png)



# 2021-04-21(padding-top: 56.25%=> 16:9 비율, youtube iframe api, gsap easing)


gsap easing
```
function floatingObject(seletor, delay, size){
  // gsap.to(요소, 시간, 옵션);
  gsap.to(seletor, random(1.5, 2.5), {
    y: size,  //y축으로 20만큼 내린다
    repeat: -1, //무한반복
    yoyo: true, //y축으로 20만큼 올린다
    ease: Power1.easeInOut,
    delay: random(0, delay)
  });
}
floatingObject('.floating1', 1, 15);
floatingObject('.floating2', .5, 15);
floatingObject('.floating3', 1.5, 20);
```


![image](https://user-images.githubusercontent.com/61581807/115522160-d5418f80-a2c6-11eb-9410-ff02c5dcd0e9.png)



# 2021-04-20(css calc, pagination, navigation)

css calc(가운데 정렬 방법)
```
.notice .promotion .swiper-container {
  width: calc(819px * 3 + 20px);
  /* width: clac(100% - 50px); */
  height: 553px;
  position: absolute;
  top: 40px;
  left: 50%;
  margin-left: calc((819px * 3 + 20px) / -2);
}
```

pagination, navigation
```
new Swiper('.promotion .swiper-container', {
  // direction: 'horizontal', // 수평 슬라이드
  autoplay: { // 자동 재생 여부
    delay: 5000 // 5초마다 슬라이드 바뀜
  },
  loop: true, // 반복 재생 여부
  slidesPerView: 3, // 한 번에 보여줄 슬라이드 개수
  spaceBetween: 10, // 슬라이드 사이 여백
  centeredSlides: true, // 1번 슬라이드가 가운데 보이기
  pagination: { // 페이지 번호 사용 여부
    el: '.promotion .swiper-pagination', // 페이지 번호 요소 선택자
    clickable: true // 사용자의 페이지 번호 요소 제어 가능 여부
  },
  navigation: { // 슬라이드 이전/다음 버튼 사용 여부
    prevEl: '.promotion .swiper-prev', // 이전 버튼 선택자
    nextEl: '.promotion .swiper-next' // 다음 버튼 선택자
  }
});
```

![image](https://user-images.githubusercontent.com/61581807/115364693-9f38d880-a1fe-11eb-9ef1-07d9e7877096.png)






# 2021-04-19(반복 애니메이션 코드(순차적) , 수직 슬라이드)

반복 애니메이션 코드

```j
//css
.visual .fade-in{
  opacity: 0;
}

//javascript
const fadeEls = document.querySelectorAll('.visual .fade-in');
fadeEls.forEach(function (fadeEl, index) {
  // gsap.to(요소, 지속시간, 옵션);
  gsap.to(fadeEl, 1, {
    delay: (index + 1) * .7, // 0.7, 1.4, 2.1, 2.8
    opacity: 1
  });
});
```

swiperjs(슬라이드 표현)

```html
<div class="notice-line">
...
  <div class="swiper-container">
    <div class="swiper-wrapper">
      <div class="swiper-slide"></div>
    </div>
  </div>
...
</div>
```

```js
<!-- new Swiper(선택자, 옵션) -->
new Swiper('.notice-line .swiper-container', {
  direction: 'vertical',
  autoplay: true,
  loop: true
});
```

![image](https://user-images.githubusercontent.com/61581807/115207755-d479f380-a136-11eb-9970-34d988ef4ee2.png)







# 2021-04-16

lodash cnd(이벤트 발생 시간 제어 라이브러리)
- _.throttle(함수, 시간);


gsap cnd(애니메이션 처리 라이브러리)
- gsap.to(요소, 지속시간, 옵션);

![1](https://user-images.githubusercontent.com/61581807/115183650-2874e000-a117-11eb-93b3-1ebe920f174d.png)

