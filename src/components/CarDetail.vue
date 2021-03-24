<template>
  <div class="car_deatail">
    <p>Марка: {{ car.brand }}</p>
    <p>Модель: {{ car.model }}</p>
    <p>Тип кузова: {{ car.body_type }}</p>
    <p>Год выпуска: {{ car.year_issue }}</p>
    <p>Пробег: {{ car.mileage }}км.</p>
    <p>Город: {{ car.city }}</p>
    <p>Описание: {{ car.description }}</p>
    <p>Коробка передач: {{ car.transmission }}</p>
    <p>Вид топлива: {{ car.fuel }}</p>
    <p>Тип привода: {{ car.drive_unit }}</p>
    <p>Объем двигателя: {{ car.engine_capacity }}см3</p>
    <p>Мощность двигателя: {{ car.engine_power }} л.с</p>
    <p>Цвет: {{ car.color_car }}</p>
    <p>Цена: {{ car.price }}$</p>
  </div>
</template>

<script>
export default {
  props:{
    car:{
      type: Object,
      required: true
    },
  }
}
</script>

<style>
.car_deatail{
  border: 1px solid black;
  padding: 10px;
}
</style>