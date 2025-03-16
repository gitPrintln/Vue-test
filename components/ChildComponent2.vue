<template>
    <div>
        <button @click="emitEvent">자식컴포넌트에서 만든 버튼</button>
    </div>
</template>

<script>
export default {
    data() {
        return{
            text: '자식컴포넌트에서 선언된 데이터입니다.',

        }
    },
    methods: {
        emitEvent(){
            this.$emit('emit-event', this.text)
        }
    },
}

</script>

<style lang="scss" scoped>

</style>