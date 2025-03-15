<template>
    <div>
        <li v-for="(item,index) in array" :key="item" @click="openDialog(index)">{{item}}/{{index}}</li>
        <router-link to="/model">v-model Page(router-link)</router-link>
        <div>
            <router-link to="/">Home</router-link>
        </div>
    </div>
</template>

<script>    
    export default {
        data() {
            return {
                array: ['a', 'b', 'c', 'd'],
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>