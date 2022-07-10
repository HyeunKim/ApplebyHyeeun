# css.md

## css

: cascading style sheets

- 사용자에게 보여주는 페이지의 꾸미는 부분

## 사용

- style 태그 내용 안에서 작성되거나,
  ```
  <style>
    body {
        background-color : red;
    }
  </style>
  ```
- body에서 사용된 태그 안에서도 사용될 수 있다
  ```
  <body>
    <p style="color: blue;">
  </body>
  ```

## 기본 속성

### 폰트 크기

- font-size : XXpx;
- px, erm

### 텍스트 정렬

- text-align: center(left/right);

### 텍스트 색깔

- color: black;

### 여백

- margin-bottom(x/left/right/top/bottom): XXpx;

## 배경

: background

### 배경 이미지

1. 삽입
   background-image: url('~~');
2. 위치
   background-position: top/left/right/bottom/50% 50%/15px 30px/...
3. 반복 x
   background-repeat: no-repeat;

cf. 배경 이비지 꽉차게 채우는 법
`width: 50px; height: 50px; background-image: url('~~'); background-size: cover;`

### 배경 색

- background-color : XX;

### id 및 class

1. id

```
#(id명) {
    내용
}
```

2. class

```
.(class명) {
    내용
}
```

### 마우스 오버

- (원하는 스타일):hover { ~~ } - 마우스 커서 위에 올라갔을 때 효과 생성
- cursor: pointer; - 마우스 커서 클릭하는 것처럼 생성
