<template>
    <div>
        <!--v-bind:포장지이름=-->
        <ChildComponent v-bind:props1="title" v-bind:props2="createAt" :props3="obj"/>
    </div>
    <div>
            <router-link to="/model2">model2 Page(router-link)</router-link>
            <div><router-link to="/">Home(router-link)</router-link></div>            
            <div><router-link to="/emit">emit test(router-link)</router-link></div>            
    </div>
</template>

<script setup lang="ts">
import {reactive, ref} from 'vue'
import ChildComponent1 from '../components/ChildComponent.vue'

interface Obj{
    id: number
    name: string
}

const title = ref<string>('부모 컴퍼넌트에서 선언된 데이터입니다.')
const createAt = ref<number>(2025)
const obj = reactive<Obj>({
    id: 2025,
    name: 'john',
})
</script>

<style lang="scss" scoped>

</style>