<template>
    <h1 class = "message">
        {{ msg }}
    </h1>
</template>

<script>
    export default{
        data(){
            return{
                msg: 'Hello SUNHO!'
            }
        }
    }
</script>

<style scoped>
    .message{
        color: red;
    }
</style>>