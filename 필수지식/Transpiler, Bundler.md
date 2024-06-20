## Transpiler

언어 대 언어로 코드를 변환하는 도구

JS ES6 → Js ES5

TypeScirpt code → JavaScript code

> 여러 브라우저 호환성을 유지하며 다양한 문법 활용 가능
> ex) Babel, SWC

### 동작 과정

1. parsing
   - 추상적인 형태의 코드로 변환하는 과정 (AST: Abstact Systax Tree)
   - AST는 scanner에 의해 분리 (탭, 공백,주석 x)
2. Transformation
   - AST를 수정하고 변환하는 단계 (설정한 플러그인에 따라 변환 => babel 등)
3. Generation
   - 변환된 AST를 js코드로 생성하는 단계 (구버전 브라우전에서 사용가능)

## Bundler

여러 개로 흩어져 있는 파일들을 압축, 난독화 하여 하나의 파일로 모아주는 도구

> 최근에는 HTML, CSS, 이미지 까지 압축하거나 최적화 함
> 기본적인 라이브러리나 프레임워크(react, next)등 에 내장되어 있지만
> 오픈소스 라이브러리를 직접 제작할 때는 직접 설정해야 한다.
> ex) Webpack, Rollup, Parcel, Vite

## 활용

[toss 트랜스파일러 활용 (로깅)](https://toss.tech/article/27750)

[toss 브라우저 번들링](https://toss.tech/article/engineering-note-6)
