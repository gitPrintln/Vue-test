<template>
    <div>
        <button v-on:click="count++">인라인 핸들러</button>
        <h1>{{count}}</h1>
        <button v-on:click="changeName">메서드 핸들러</button>
        <h1>{{name}}</h1>
        <h1>{{text}}</h1>
        <h1>changeText 함수 호출: {{changeText()}}</h1>
        <h1>changeText 함수 호출: {{changeText()}}</h1>
        <h1>changeText 함수 호출: {{changeText()}}</h1>
        <h2>computedText 호출: {{computedText}}</h2>
        <h2>computedText 호출: {{computedText}}</h2>
        <h2>computedText 호출: {{computedText}}</h2>

        <button @click="changeMessage">{{message}}</button>
        {{watchMessage}}
    </div>
    <div>
            <router-link to="/data">data Page(router-link)</router-link>
            <div><router-link to="/">Home(router-link)</router-link></div>            
    </div>
</template>

<script>
    export default {
        data() {
            return {
                count:0,
                name:'vue.js',
                text:'Computed 텍스트 데이터 문구입니다.',
                message:'안녕하세요, Watch 기능 테스트 오리지널 문구',
                watchMessage: '',
            }
        },
        watch: {
            // message: function(){} 형태
            // 데이터 뿐만아니 라 computed로 계산된 데이터로 watch 감지가능
            // 보통 게시판에서 한컬럼 선택했을 경우 , 고유한 id 값이 바뀜을 확인
            // 이 때 그 id값에 따른 상세 데이터를 호출할 때 주로 사용한다.
            message() {
                // window.alert("message 변수에 담긴 데이터가 변경되었습니다.")
                this.watchMessage = 'Watch 동작'
            },
            id() {
                //해당 상세 데이터를 조회하는 api 호출
            }
        },
        // methods 부분에 선언된 함수와 동일한 로직일 때
        // 캐싱기능이 없는 methods는 호출될 때마다 console 값이 출력되었습니다.
        // computed는 캐싱기능이 있기 때문에 methods와 어떤 차이점이 있는지..
        computed: {
            computedText() {
                console.log('computed 기능을 생성함')
                return this.text.split('').reverse().join('')
            },
        },
        methods: {
            changeName() {
                this.name = '변경된 텍스트입니다.'
            },
            changeText() {
                console.log('changeText()')
                console.log(this.text)
                return this.text.split('').reverse().join('')
            },
            changeMessage() {
                console.log('changeMessage()')
                this.message = '변경된 message 데이터입니다.'
            },
        },
    }
</script>

<style lang="scss" scoped>

</style>