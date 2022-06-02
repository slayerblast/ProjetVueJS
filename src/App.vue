<script setup>
import {ref} from "vue"
const cle = ref(0)
setInterval(()=>{
  cle.value++
}, 1000)
function decryptCle(){
  cle.value = 0;
}
</script>

<template>
<h1>DECRYPTEUR</h1>
<button @click="decryptCle()">mettez la clé</button>
<input type="number" v-model="cle">
<p>{{cle}}</p>
</template>