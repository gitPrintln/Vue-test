<template>
    <div>
        <input type="text" v-model="inputValue1" />
        <input type="text" :value="inputValue2" @input="inputValue2 = $event.target.value" />
        <!-- onchange, onInput >> v-on >> @ 로 사용 -->
        <!-- 한글을 입력할 때 input1은 한템포 느리게 되는데, input2는 바로바로 입력됨-->
        
    </div>
    <div>{{inputValue1}}</div>
    <div>{{inputValue2}}</div>
</template>

<script>
    export default {
        data() {
            return{
                inputValue1: '',
                inputValue2: '',
            }
        },
        
    }
</script>

<style lang="scss" scoped>

</style>