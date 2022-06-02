<script setup>
import {ref} from "vue"
import * as jose from 'jose'

let cle = ref()
let claims = ref()

function decryptCle(){
console.log(cle.value)
claims = jose.decodeJwt(cle.value)
console.log(claims)


}
</script>

<template>
<h1>DECRYPTEUR</h1>
<button @click="decryptCle()">mettez la clé</button>
<input type="text" v-model="cle">

<p>{{cle}}</p>
</template>