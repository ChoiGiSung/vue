<template>
  <div>
  <!-- v:bind: 프롭스 속성 이름 = "상위 컴포넌트의 데이터 이름 "-->
    <app-header 
    v-on:renew="renewStr"
     v-bind:propsdata="str"></app-header>
  </div>
</template>

<script>
  import AppHeader from './components/AppHeader.vue';


  export default {
  components: { AppHeader },
    data:function(){
      return{
        str: 'hi'
      }
    },
    Comments:{
      'app-header' : AppHeader
    },
    methods:{
      renewStr:function(){
        this.str = 'header'
      }
    }
  }
</script>

<style>


</style>
