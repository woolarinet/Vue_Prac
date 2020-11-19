# v-html  
문자열 데이터 안의 html코드를 제대로 출력 시키기 위한 디렉티브  
    [^1]: <div v-html = "msg"></div>  형태로 사용
# v-bind  
특정 속성을 binding하기 위한 디렉티브  
    [^2]: <div v-bind: class = "class"></div> 의 형태  'v-bind:' 는 ':'로 축약 가능
# v-slot  
컴포넌트를 화면에 렌더링할 때 컴포넌트 안의 특정 컨텐츠는 렌더링 되지 않는다.  
이 때 이걸 가능하게 해주는 디렉티브  
    [^3]: > template: '<div><slot></slot></div>' 의 형태로 기본적으로 이 컴포넌트 안에는 특정 컨텐츠가 렌더링이 가능해진다.  
    > 111
