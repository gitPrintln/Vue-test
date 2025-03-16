<template>
  <h1>Vue.js 테스트</h1>
  <div>{{ rawHTML }}</div>
  <div>{{ rawHTML2 }}</div>
  <h1 v-html="rawHTML2"></h1>

  <h2 v-bind:class="{active: isActive}">class binding test</h2>
  <h2 :class="{active: isActive}">class binding test</h2>
  <button @click="change">버튼</button>

  <h3 style="color: red; font-size: 20px;">style binding test</h3>
  <h3 :style="{color: fontColor, fontSize: fontSize + 'px' }">style binding test</h3>
  <router-link to="/home2">v-if,v-show Page(router-link)</router-link>
  <div>
  <button @click="goToHome2">v-if,v-show Page(SPA방식)</button>
  </div>
  <div>
    <router-link to="/toast">toast gogo</router-link>
  </div>
</template>

<script>
export default {
  data() {
    return{
      rawHTML: '이것은 텍스트입니다.',
      rawHTML2: '<span style="color: red"> 이것은 빨간색입니다.</span>',
      isActive: false,
      fontColor: '#888888',
      fontSize: 30,
    }
  },
  methods: {
      change() {
        this.isActive = !this.isActive
      },
      goToHome2() {
        this.$router.push("home2");
      },
  },
}
</script>

<style>
h2.active{
  color: green;
}
</style>