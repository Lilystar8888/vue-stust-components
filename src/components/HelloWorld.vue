<template>
  <div class="hello">
    <h1>{{counter}}</h1>
    <button @click="addCount">Add</button>
  </div>
</template>

<script>
export default {
  data(){
    return {
      count: 0,
    };
  },
  methods:{
    addCount(){
      this.count+=1;
    },
  },
};
</script>

<style scoped>
.counter {
  color: red;
}
</style>
