<template>
  <div>
    <Car :car = "car" @setCar = 'setCar'/>
  </div>
</template>

<script>
import Car from '@/components/Car.vue'
import axios from "axios"
export default {
  data() {
    return {
      car: [],
    }
  },
  components: {
      Car
  },
  mounted() {
    axios.get('http://127.0.0.1:8000/car/')
        .then(response => this.car = response.data);
  },
  methods: {
    setCar(val) {
      axios.post('http://127.0.0.1:8000/сar/', val)
          .then(response => this.car = response.data);
      console.log(this.car)
    }
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
</style>
