# starbucksDema

# ご覧になる方法

![2](https://user-images.githubusercontent.com/61581807/115183963-c9fc3180-a117-11eb-864d-5f92721d9798.png)


ダウンロードにした圧縮ファイルの解凍をしてください。



![3](https://user-images.githubusercontent.com/61581807/115184098-16e00800-a118-11eb-8c93-c1d0d7e5ab86.png)




# 2021-04-19

반복 애니메이션 코드

```j
//CSS
.visual .fade-in{
  opacity: 0;
}

//JS
const fadeEls = document.querySelectorAll('.visual .fade-in');
fadeEls.forEach(function (fadeEl, index){
  // gsap.to(요소, 지속시간, 옵션);
   gsap.to(fadeEl, 1, {
     delay: (index + 1) * .7, // 0.7, 1.4, 2.1, 2.8
     opacity: 1
   });
});
```

![image](https://user-images.githubusercontent.com/61581807/115199255-fc188e00-a12d-11eb-8532-5c11d3dd4587.png)





# 2021-04-16

lodash cnd(이벤트 발생 시간 제어 라이브러리)
- _.throttle(함수, 시간);


gsap cnd(애니메이션 처리 라이브러리)
- gsap.to(요소, 지속시간, 옵션);

![1](https://user-images.githubusercontent.com/61581807/115183650-2874e000-a117-11eb-93b3-1ebe920f174d.png)

