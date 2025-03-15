<template>
    <div>
        <div>{{props1}}</div>
        <div>{{props2}}</div>
        <div>{{props3.id}}</div>
        <div>{{props3.name}}</div>
    </div>
</template>

<script>
    export default {
        props: {
            props1: String,
            props2: Number,
            props3: Object,
        },
        data() {
            return {}
        },
    }
</script>

<style lang="scss" scoped>

</style>