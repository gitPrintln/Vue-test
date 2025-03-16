<template>
    <div>
        <button @click="emitEvent">자식컴포넌트에서 만든 버튼</button>
    </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'
// 반응성을가진(변화를 가진) ref를활용해주는게 좋음

const data = ref<string>("자식컴포넌트에서 선언된 데이터입니다.")
// props는 전달할 포장지 이름을 정해줬다면, emit는 전달할 이벤트 포장지 이름을 정해줌
const emit = defineEmits(['emit-event'])
const emitEvent = () => {
    // data.value => composition api에서 ref속성을 참조해서 원래 본래 값을 가져옴
    emit('emit-event', data.value)
}
</script>

<style lang="scss" scoped>

</style>