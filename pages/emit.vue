<template>
    <div>
        부모컴퍼넌트 레이아웃
        <ChildComponent2 @emit-event="parentEvent" />
    </div>
</template>

<script>
import ChildComponent2 from '../components/ChildComponent2.vue'


export default {
    components: {
        ChildComponent2,
    },
    methods: {
        parentEvent(event) {
            console.log(event)
        },
    },
}
</script>

<style lang="scss" scoped>

</style>