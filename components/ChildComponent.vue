<template>
    <div>
        <div>{{props.props1}}</div>
        <div>{{props.props2}}</div>
        <div>{{props.props3.id}}</div>
        <div>{{props.props3.name}}</div>
    </div>
</template>

<script setup lang="ts">
import { toRefs } from 'vue'

interface Obj{
    id: number
    name: string
}

// composition API
// prop 받은 데이터 형식에 맞게 타입을 지정해준다.
// prop 받은 데이터 이름 자체에 미리 선언해둔 타입을 설정해둔다. 위의 Obj
interface Props {
    props1: String,
    props2: Number,
    props3: Obj,
}

// define props toRefs 내장함수를 통해 prop 받은 데이터를 활용하여 템플릿에서 호출하여 사용
const props = defineProps<Props>()
// 명시적으로 윗부분 import 해줘야함
const { props1, props2, props3} = toRefs(props)
</script>

<style lang="scss" scoped>

</style>