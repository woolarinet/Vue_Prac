# 전처리 -> CSS -> 후처리

## 전처리
    LESS, SASS(SCSS), Stylus, PreProcessor

## 후처리
    Postcss -> 크롬, 파이어폭스, IE, 오페라등의 접두사(Webkit, ms, etc)를 통해 표준이 아닌 문법을 지원

### 로더 설치 문제점
    sass-loader의 현재 버전을 설치 시에는 추가적인 모듈 설치가 필요한데, 아직 이해가 부족하여 7버전으로 설치를 하였고,
    그에 맞게 node-scss의 버전도 4로 낮춰서 설치하였다.
    postcss의 경우에도, autoprefixer의 버전에 호환되는 Postcss가 아직 릴리스되지 않아 autoprefix의 버전도 9로 낮춰 설치 하였다.
    
### 설치 후 npm run dev를 통해 본 결과, style태그에 설정했던 display: flex; 속성을 통하여 
                     h1태그의 webkit, ms의 flex 속성이 postcss의 flex로 대체 되었다.
                     
                 
