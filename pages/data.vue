<template>
    <div>
        <!--v-bind:포장지이름=-->
        <ChildComponent v-bind:props1="title" v-bind:props2="createAt" :props3="obj"/>
    </div>
</template>

<script setup lang="ts">
import ChildComponent from '@/components/ChildComponent.vue'

const title = ref<string>('부모 컴포넌트에서 선언된 데이터입니다.')

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