<template>
  <div>
        <!-- <div v-if="isVisible" class="red"></div>
        <div v-if="isVisible === true" class="green"></div>
        <div v-else class="blue"></div> -->
        <!-- <div v-if="count > 1" class="red"></div>
        <div v-else class="blue"></div> -->

        <!-- <button @click="count++">count ++</button>
        <button @click="count--">count --</button> -->

        <div v-show="isVisible" class="red"></div>
        <div v-show="!isVisible" class="green"></div>
        <div v-if="isVisible" class="blue"></div>
        <router-link to="/list">v-list Page(router-link)</router-link>
        <div>
            <router-link to="/">Home</router-link>
        </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            isVisible: false,
            count: 0,
        }
    },

}
</script>

<style>
.red {
    width: 100px;
    height: 100px;
    background-color: red;
}
.green {
    width: 100px;
    height: 100px;
    background-color: green;
}
.blue {
    width: 100px;
    height: 100px;
    background-color: blue;
}
</style>