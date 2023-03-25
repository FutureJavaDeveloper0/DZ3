<script setup>
import {ref} from "vue";
import style from "./cardStyle.module.css";

const cars = ref([
  {car: "Toyota"},
  {car: "BMW"},
  {car: "Mercedes"},
  {car: "Lamborghini"},
  {car: "Tokada"},
]);
// const cars = ref(["car1","car2","car3"]);
const text = ref("");

</script>

<template>
  <input type="text" v-model="text"/>
  <template  v-for="{car} in cars" :key="car.value">
    <div  :class = "style.car" v-if="car.toLowerCase().includes(text.toLocaleLowerCase())">
      <h1>{{ car }}</h1>
    </div>
  </template>
</template>
