<script setup>
import { ref } from "vue";

import style from "./Card.module.css";


const quantity = ref(5000);

// watch(quantity, () => {
//     if (quantity == 0) {
//         quantity = 0;
//     }
// })

</script>

<template>
    <div >
        <button @click="quantity--" ><slot :quantity="quantity">Bum</slot></button>
    </div>
</template>
