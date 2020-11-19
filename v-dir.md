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

 
