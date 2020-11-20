# v-html  
문자열 데이터 안의 html코드를 제대로 출력 시키기 위한 디렉티브  
```
<div v-html = "msg"></div> 
```
의 형태로 사용
# v-bind  
특정 속성을 binding하기 위한 디렉티브  
```
<div v-bind: class = "class"></div>
```
의 형태  'v-bind:' 는 ' : '로 축약 가능
# v-slot  
컴포넌트를 화면에 렌더링할 때 컴포넌트 안의 특정 컨텐츠는 렌더링 되지 않는다.  
이 때 이걸 가능하게 해주는 디렉티브  
```
Vue.component('my-comp',{
    template: '<div><slot></slot></div>'
    })
```
의 형태로 기본적으로 이 컴포넌트 안에는 특정 컨텐츠가 렌더링이 가능해진다.  
```
'<div><slot name = "slot1"></slot></div>'
```
은 특정 슬롯이름을 부여해 각 컨텐츠를 슬롯 이름에 맞게 렌더링이 가능해진다.  
## slot-scoped  
슬롯에 속성을 추가했을 때, 부모컴포넌트에서 쓸 수 있게 해준다.  
```
<body>
    <div id = "app1">
        <j-c>
            <template slot-scope = "{ mySlotData }">
                {{ mySlotData }}
            </template>
        </j-c>
    </div>
</body>
<script>
        Vue.component('j-c',{
            template : '<div> <slot :my-slot-data = "message"> </slot> </div>',
            data(){
                return{
                    message: 'Hello Slot~'
                }
            }
        })
</script>
```  
의 형태로 작성. 슬롯의 속성인 message가 템플릿 내부에 담게 된다.  
# v-once  
한번만 렌더링  
```
<div v-once>{{ msg }}</div>
```  
# v-model  
양방향 바인딩을 위한 디렉티브  
```
<input type = "text" v-model = "message">
<div>{{ message }}</div>
``` 
의 형태. 실시간으로 바뀌는 것이 아닌, 모두 입력 후 바뀌길 원한다면  
```
<input type = "text" v-model.lazy = "message">
```
문자 맨 앞, 혹은 뒤의 공백을 자동으로 없애주는 trim
```
<input type = "text" v-model.trim = "message">
```
입력 값을 자동으로 숫자로 바꿔주는 number
```
<input type = "text" v-model.number = "message">
```  
# v-if, v-show  
조건부 렌더링 디렉티브. 
둘다 같은 동작이지만, v-if 는 토글 비용이 높고, v-show는 초기 렌더링 비용이 높다.  
자주 바꾸길 원하면 v-show, 런타임 시 조건이 크게 바뀌지 않는다면 v-if를 쓰자!  
```
<div v-if = "show"
     class = "box"></div>     (v-if)
<div v-show = "show"
     class = "box"></div>     (v-show)
```
