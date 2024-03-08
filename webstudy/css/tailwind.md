* Tailwind CSS
CSS스타일을 사용하는 것 만큼 쉽고 빠르게 스타일링 할 수 있음 + 일관된 디자인 가능하게 함 깃허브랑 Nuxt.js에서도 사용중

* 설치
1. 터미널 설치
```
npm install tailwindcss@latest postcss@latest autoprefixer@latest
```
2. PostCSS 플러그인에 추가
```
// postcss.config.js 등의 postcss 설정 파일
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
};
```
3. 설정 파일 생성
```
npx tailwindcss init
```
```javascript
// tailwind.config.js
module.exports = {
  purge: [],
  darkMode: false, // or 'media' or 'class'
  theme: {
    extend: {},
  },
  variants: {},
  plugins: [],
};
```

* tailwind css 스타일 추가
```css
/* css */
@tailwind base;
@tailwind components;
@tailwind utilities;
```
```typescript
// react script app.tsx
import "tailwindcss/tailwind.css"
```

* 최적화
purge 옵션 사용 -> 프로덕션 빌드할 때 파일에서 사용하지 않는 클래스는 전부 제거해줌
```javascript
// tailwind.config.js
module.exports = {
  purge: ['./src/**/*.{js,jsx,ts,tsx}'],
  ...
}
```

* 기본 설정 커스텀 가능
추가 설명(https://tailwindcss.com/docs/configuration)
```javascript
// tailwind.config.js
module.exports = {
  theme: {
    colors: {
      gray: colors.coolGray,
      blue: colors.lightBlue,
      red: colors.rose,
      pink: colors.fuchsia,
    },
    fontFamily: {
      sans: ["Graphik", "sans-serif"],
      serif: ["Merriweather", "serif"],
    },
    extend: {
        colors: {
        primary: '#8ffebf',
        },
    },
    variants: {
        extend: {
        borderWidth: ['hover'],
        },
    },
  },
};
```
기본 스타일을 설정할 때, 기본 스타일 값을 오버라이딩 하지않게 extends 객체 안에 넣어주는 것 중요!

* 장점
- Utility-First 컨셉을 가진 CSS 프레임워크
부트스트랩처럼 클래스에 태그를 붙여 속성을 추가하는 사용이 가능하다.
- 로우레벨 스타일 제공
각 css의 요소에 유틸리티 클래스가 제공돼 간단한 기술로 디자인 구현 가능
- Intelli Sense 플러그인 제공
로우레벨, 유틸리티 클래스의 미리보기나 자동완성이나 기타 기능들이 지원된다
- JS 코드와 분리되어 있어 프레임워크를 변경해도 큰 추가작업이 필요 없다.

* 단점
- 클래스 명이 좀 길다
- JS코드 사용이 어렵다. 자바스크립트 변수 값에 따라 기능이 들어가는 구현은 가능하나 번거로워진다.

참고 (https://wonny.space/writing/dev/hello-tailwind-css)