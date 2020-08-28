<template>
  <div id="app">

    <div v-for="(tax, index) in taxes" :key="index">
      <copy />
    </div>

    <p>

    <div class="add">
      <vs-button
        shadow
        :active="active == 1"
        @click="add"
      >
      Add New Line
      </vs-button>
    </div>
    
    <!-- <p>Count: {{taxes.length}}</p> -->

    </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import Copy from './components/Copy.vue'

export default {
  name: 'App',
  data() {
    return {
      taxes: [0],
      active: 1
    }
  },
  methods:{
    add: function(){
      this.taxes.push(0);
    }
  },
  components: {
    //HelloWorld,
    Copy
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.add {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  /* height: 100vh; */
}
</style>
