<script setup>
import {ref} from "vue"
import * as jose from 'jose'

let cle = ref()
let claims = ref(null)

function decryptCle(){
console.log(cle.value)
claims.value = jose.decodeJwt(cle.value)
console.log(claims)
}

function saveCle(){
  localStorage.setItem('jwt',cle.value)
}
const savedCle = ref('')
function loadSavedCle(){

}
</script>

<template>
<h1>DECRYPTEUR</h1>
<button @click="decryptCle()">mettez la clé</button>
<input type="text" v-model="cle">

<p>{{claims}}</p>

<button @click="saveCle()"> </button>
</template>