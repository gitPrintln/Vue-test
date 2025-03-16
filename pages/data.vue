<template>
    <div>
        <!--v-bind:포장지이름=-->
        <ChildComponent v-bind:props1="title" v-bind:props2="createAt" :props3="obj"/>
    </div>
    <div>
            <router-link to="/model2">model2 Page(router-link)</router-link>
            <div><router-link to="/">Home(router-link)</router-link></div>            
    </div>
</template>

<script>
import ChildComponent from '@/components/ChildComponent.vue'
export default {
        components: {
            ChildComponent,
        },
        data() {
            return {
                title: '부모 컴퍼넌트에서 선언된 데이터입니다.',
                createAt: 2025,
                obj:{
                    id: 2025,
                    name: 'john',
                },
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>