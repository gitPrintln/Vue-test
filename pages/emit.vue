<template>
    <div>
        부모컴퍼넌트 레이아웃
        <ChildComponent2 @emit-event="parentEvent" />
    </div>
</template>

<script setup lang="ts">
import ChildComponent2 from '../components/ChildComponent2.vue'

const parentEvent = (event: string) => {
    console.log(event)

}

</script>

<style lang="scss" scoped>

</style>