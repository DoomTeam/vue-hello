<template>
<div>
<p>this is a info</p>
<button type="button" @click="add()">添加</button>
</div>
</template>
<script>
import store from '@/store'
export default {
  name:"Info",
  store,
  data(){
    return{
      msg:'hello world'
    }
  },
  mounted(){
    window.vue = this
  },
  methods:{
    add(){
      console.error('handler event')
      store.commit('increate')
    },
    output(){
      console.log('in output')
    }
  }
}
</script>

<style scoped>
</style>