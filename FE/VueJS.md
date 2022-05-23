## vue 환경설정

- vue-cli?
    - 일반적인 프로젝트 구조와 개발환경으로 새 프로젝트를 생성할 수 있도록 도와줌

```bash
npm install vue-cli -g
#todo-client라는 프로젝트를 webpack 템플릿으로 생성한다
vue init webpack todo-client
#이후 옵션 설정
cd todi-client
npm install
npm run dev
#localhost:8080 에서 페이지 확인 가능
```

⇒ 여기까지 하면 프로젝트 기본적으로 확인 가능

npm run dev 가 띄워져 있으면 서버 재기동 없이도 변경사항이 바로 페이지에 적용

- index.html 은 가급적이면 수정하지 않을 것

- App.vue 수정
    - vue는 템플릿, 스크립트, 스타일로 구성

- router/index.js 수정
    - 서버에서만 사용하던 라우터를 프론트엔드에서도 사용할 수 있도록 함
    - 새 컴포넌트를 사용하려면 components/ 에 새 컴포넌트를 생성하고, router에 해당 컴포넌트를 import하여 사용

[http://localhost:8080/#/example](http://localhost:8080/#/example) → 왜 중간에 #이 들어가지…

5번부터 마저 따라하기

[https://blog.storyg.co/vue-js-posts/todos-tutorial](https://blog.storyg.co/vue-js-posts/todos-tutorial)
