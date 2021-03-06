# em

em 은 **이 단위가 적용된 엘리먼트의 글자 크기에 비례**한다.
em 은 적용되어 있지만 글자 크기가 적용되어 있지 않아서 부모의 값을 받아오는 경우,
(font-size 는 상속형 속성이다) 부모의 글자 크기를 물려받아 자식의 글자 크기가 **“먼저”** 적용되고, 그 후에 em에 적용된다.

### 장점

픽셀에 비해선 상대적으로 더욱 유연하게 처리할 수 있어서 조건에 맞게 length 를 조절할 수 있다.

### 단점

em은 자기 자신의 글자 크기를 참조하기 때문에, **em 을 사용하는 다른 속성 역시 글자 크기에 영향을 받을 수 밖에 없다!**
또한, 글자 크기가 변하지 않더라도 부모의 글자 크기가 변하면 또 복잡하게 일이 흘러갈 수도 있다.
➡️그렇기에 필요한 곳에만 사용할 것!





# rem

rem 역시 em 과 마찬가지로 글자 크기에 따라 비례되는 속성인데,
오직 **html 태그의 글자 크기만 참조**한다.
**다른 모든 태그의 글자 크기는 신경쓰지 않는다.**

rem을 사용할 경우, 계산하기 쉽게 참조 대상의 글자 크기를 10 픽셀로 맞춰놓고 진행하는 경우가 많다.
html 태그의 경우, 브라우저 기본 설정 기준에서 기본 16 픽셀을 갖고 시작하는데 여기에 62.5% 를 곱해주면 10 픽셀로 맞춰놓고 시작할 수 있다.

```null
html {
font-size: 62.5%;
}
```

이러면 html 은 10 픽셀로 맞춰지게되고, 하위 태그에서 rem 을 사용하는 경우 10 배수로 계산하면 되니 훨씬 편하다.





# Px

Picture Element의 약자로 우리말로는 화소라고 한다.
화면의 이미지를 구성하는 최소의 단위를 말하며, 사각형으로 이루어져있으며 해상도를 나타낸다.
픽셀의 수가 많아질수록 고해상도의 이미지라고 말한다.

**픽셀은 DPI의 값에 따라 얼마든지 달라질 수 있다.** 즉 물리적인 크기로 나타낼 수 없다.
96 DPI와 360DPI에서의 1px는 다르다.