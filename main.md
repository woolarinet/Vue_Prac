# main
##### 최상위 컴포넌트의 진입점
##### 최상위 컴포넌트에 연결되어 있는 수많은 하위 컴포넌트들을 구조로 가지고 있다.
<img width="336" alt="스크린샷 2020-11-18 오전 2 17 00" src="https://user-images.githubusercontent.com/66486641/99423965-79a05e00-2944-11eb-8ce4-7889d23300dd.png">

## Example

> new Vue({  
　  el: '#app',  
　  router,  
　  // 뷰 인스턴스에 최초연결을 위한 함수  
　  // h는 createElement의 축약형  
　  render: h => h(App)  
> })  


렌더 부분은    
> 　render: (createElement) {  
   　　return createElement(App)  
>　 }  

이 형태를 뷰의 문법으로 나타낸 것이다  
