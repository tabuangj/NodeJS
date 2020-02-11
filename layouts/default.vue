<template>
  <div>
      <input type="text" v-model="dataIN"/>
     <button v-on:click="checkForm()">Add</button>
    <div v-for="(row, i) in output" :key="i">
      <label>{{row.inputname}}</label>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      dataIN:'',
      output:[]
    }
  },
  methods:{
    checkForm(){  
       this.output.push({inputname: this.dataIN})
    }
  }
}
</script>

<style>
</style>
