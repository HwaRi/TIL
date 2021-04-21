# srcset?
같은 비율의 이미지를 여러 크기로 다른 환경에서 사용할 수 있도록 소스에 명시하는 것.  
브라우저가 최적 크기의 이미지를 선택하도록 함.
  
+ 다른 비율의 다양한 크기 이미지를 사용하고 싶은 거라면 css의 @media 사용을 확인할 것.

### 구성
"{이미지 URL} {너비 descriptor 또는 픽셀 밀도 descriptor}, 반복..."
1. 이미지 URL : 사용할 이미지 URL
2. 이미지 URL과 descriptor 사이에는 공백 필요
3. 너비 descriptor(w descriptor) : 양의정수w의 형식. 이미지의 가로 너비를 명시.
5. 픽셀 밀도 descriptor(pixel density descriptor) : 양의 부동소수점 수x. 배율을 명시. default 1x.

### 사용 예시
``` html
<img srcset="{960 image URL} 960w,
             {575 image URL} 575w"
     sizes="(min-width: 960px) 50vw,
            (min-width: 575px) 75vw,
            100vw"
     src="{default image URL}" alt="{alter text}">
```
```
<img srcset="{이미지 경로} 너비w,
             {이미지 경로} 너비w"
     sizes="{(미디어조건)} 최적화출력크기,
            {(미디어조건)} 최적화출력크기,
            기본출력크기"
     src="{경로}" alt="{대체 문구}">
```
- 이미지 경로 입력 시 작은 크기부터 순서대로 입력
- w descriptor 사용 시 브라우저가 각 이미지의 최적화된 픽셀 밀도를 계산하여 적합한 이미지 사용.
  - 뷰포트 너비에 따라 변경
- x descriptor 사용 시 디바이스의 픽셀 비율과 일치하는 최적화된 이미지 사용.
- width vs sizes
  - width는 출력 크기 지정. sizes는 출력 크기와 최적 크기도 지정

#### 지원 브라우저 및 버전
* IE 지원하지 않음  

|브라우저|버전|
|----|---|
|chrome|34.0|
|edge|지원|
|forefox|38.0|
|safari|8.0|
|opera|21.0|
