<template>
  <div>
    <div class="search">
      <select v-model="selected">
        <option disabled value="">Выберите марку авто</option>
        <option>Mazda</option>
        <option>Chevrolet</option>
      </select>
      <p>{{ selected }}</p>
    </div>
    <CarDetail
        v-for="car of car" :key="car"
        v-bind:car="car"
    />
  </div>
</template>

<script>
import CarDetail from '@/components/CarDetail'
export default {
  data(){
    return {
      selected: ''
    }
  },
  props:[
      'car'
  ],

  components:{
    CarDetail
  },
  watch: {
    selected(val) {
     this.$emit('setCar', val);
    }
  }
}
</script>

<style>

</style>